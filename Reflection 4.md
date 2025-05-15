## PRACTICAL 1 : File Upload Implementation

### Key Concepts Applied

1. **React Hook Form**
   - Used for form handling and validation.
   - Integrated file input with validation rules.

2. **Formidable**
   - Used on the backend to handle `multipart/form-data`.

3. **Axios**
   - Used to send POST requests and track upload progress using `onUploadProgress`.

4. **React Dropzone**
   - Implemented drag-and-drop file upload UI.

5. **Validation**
   - Files limited by type (`.jpg`, `.png`, `.pdf`)
   - Max file size check (e.g., 5MB)

6. **Upload Progress**
   - Real-time progress bar updates as the file uploads

### What I Learned

- How to handle file uploads with validation in a React/Next.js app
- How to use `formidable` for parsing file uploads on API routes
- Integration of drag-and-drop UI using `react-dropzone`
- Tracking upload progress using Axios and displaying a progress bar
- Structuring a full-stack file upload solution in a Next.js project

### Challenges Faced

#### 1. Formidable Parsing Error
**Problem:** Initial attempt to parse `multipart/form-data` failed with an internal error.  
**Solution:** Disabled body parsing using:
```js
export const config = {
  api: {
    bodyParser: false,
  },
};
```

#### 2. Drag and Drop Events Not Triggering
Problem: Drag events were not being registered.
Solution: Correctly applied props from useDropzone():
```js
{...getRootProps()}
{...getInputProps()}
```

#### 3. Axios Progress Bar Not Updating
Problem: onUploadProgress wasn't triggering properly.
Solution: Ensured correct config and passed to Axios POST request:
```js
onUploadProgress: (progressEvent) => {
  const percent = Math.round((progressEvent.loaded * 100) / progressEvent.total);
  setProgress(percent);
}
```
