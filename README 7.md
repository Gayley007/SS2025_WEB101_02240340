## Practical 7 – Data Visualization Dashboard in React

### Project Overview
This practical focuses on building an **analytics dashboard** using **React** and popular **charting libraries** like **Recharts** and **react-chartjs-2**. The project visualizes different datasets through various chart types to provide insight into business metrics.

### Setup Instructions

#### Step 1: Clone Starter Repository
```bash
git clone https://github.com/syangche/Data-Visualisation.git
cd Data-Visualisation
npm install
npm run dev
```

#### Step 2: Install Chart Libraries
```bash
npm install recharts
npm install chart.js react-chartjs-2
```

### Implemented Charts
1. MonthlySalesChart.jsx
▫️Library: Recharts <br>
▫️Type: Line Chart <br>
▫️Use Case: Display monthly sales trends <br>
▫️Props Used: dataKey, CartesianGrid, Tooltip, ResponsiveContainer

2. ProductCategoryChart.jsx
▫️Library: Recharts <br>
▫️Type: Pie Chart <br>
▫️Use Case: Show distribution of products across categories

3. CustomerAcquisitionChart.jsx
▫️Library: react-chartjs-2<br>
▫️Type: Bar Chart<br>
▫️Use Case: Display monthly customer acquisition rate

4. WeeklyVisitorsChart.jsx
▫️Library: react-chartjs-2 <br>
▫️Type: Area Chart <br>
▫️Use Case: Visualize website traffic across a week

### Key Concepts
- Using multiple charting libraries in one project
- Making charts responsive with ResponsiveContainer
- Data-driven chart rendering
- Chart component reusability
- Handling external or mock data for real-time analytics UI
