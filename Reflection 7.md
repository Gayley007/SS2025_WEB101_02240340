## PRACTICAL 7: Data Visualization

### Key Concepts Applied

1. **Charting Libraries Integration**
   - Integrated **Recharts** for line and pie charts
   - Used **react-chartjs-2** with **Chart.js** for bar and area charts

2. **Component-Based Chart Design**
   - Modular chart components for reusability and maintainability
   - Each chart is separated into its own JSX file

3. **Responsive and Interactive Charts**
   - Wrapped charts in `ResponsiveContainer` to support different screen sizes
   - Enabled interactivity via tooltips and legends

4. **Data Preparation**
   - Simulated real-world datasets (e.g., sales, visitors, acquisitions)
   - Structured the data into objects and arrays suited for charting


### What I Learned

- How to use **multiple charting libraries** in a single React project
- Creating responsive dashboards that adapt across devices
- Choosing the right chart type for different data narratives
- Structuring and transforming data for visualization components
- Troubleshooting layout and rendering issues in dynamic charts


### Challenges Faced

#### 1. Chart Not Rendering
**Problem:** `react-chartjs-2` chart remained blank  
**Solution:** Ensured `Chart.js` was properly registered and wrapped chart data and options correctly.

#### 2. Layout Overflow on Small Screens
**Problem:** Chart widths exceeded screen size  
**Solution:** Wrapped charts with `ResponsiveContainer` and used `flex-wrap` and `minWidth` in parent containers.

#### 3. Mismatched Data Keys
**Problem:** Incorrect `dataKey` caused blank charts  
**Solution:** Double-checked that the data object structure matched the expected keys in chart props.
