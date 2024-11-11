# Bike Buyers Dashboard Project

Welcome to my **Bike Buyers Dashboard Project**—an interactive Excel dashboard crafted from real data, transformed and visualized to extract meaningful insights. As my second foray into Excel project building, this one is a bit more straightforward than my previous project. However, my goal was to ensure I could revisit key concepts and continue refining my data skills.

Through this project, I’m focused on effective data cleaning, Power Query transformations, and dashboarding techniques. From handling data transformations to building an interactive dashboard, I focused on creating a tool that’s both informative and easy to use for exploring buying patterns among different groups. Here’s a step-by-step breakdown of what I achieved:

## 📈 Insights Discovered

Through this analysis, I observed several interesting patterns:
- **Income Influence**: On average, customers who purchased a bike had a slightly higher income, with male customers in particular showing a significant difference between those who bought and those who didn’t.
- **Distance from Store**: Proximity played a role in purchase likelihood; customers closer to the store were more likely to buy a bike.
- **Age Group Trends**: The "Middle Age" group had the highest purchase count, suggesting they are the primary target demographic, while younger "Adolescents" and older "Seniors" had comparatively fewer purchases.

## 🎯 Project Goals and Workflow

### 1. **Data Cleaning and Transformation in Power Query**
   
 **Starting in Power Query**, I went through essential data transformations to prepare the dataset for analysis. Here are the key steps I took:
   
   - **Remove Duplicates**: Ensured data accuracy by removing duplicate rows, eliminating inconsistencies.
   - **Standardize Column Values**:
     - **Marital Status**:  Translated "M" to "Married" and "S" to "Single" for clarity.
     - **Gender**: Transformed "M" to "Male" and "F" to "Female".
   - **Format Conversion**:
     - Converted **Income** values into currency format (Dollar) to facilitate financial analysis.
   - **Age Grouping**: Categorized age into meaningful groups for demographic insights. Here’s the custom formula I used:
     
     ```powerquery
     = Table.AddColumn(#"Format Conversion", "Age Brackets", each 
          if [Age] < 31 then "Adolescent" 
          else if [Age] >= 31 and [Age] <= 55 then "Middle Age" 
          else if [Age] > 55 then "Senior" 
          else null
     )
     ```

### 2. **Loading Data to Excel and Building Visualizations**

   After transforming the data, I loaded it back into Excel to build **Pivot Tables** and **Charts** for deeper analysis. This included:

   - **Average Income by Gender and Bike Purchase Status**:
     
   ![image](https://github.com/user-attachments/assets/80e84819-cc71-40f7-a117-743d4d212c5c)

   - **Bike Purchase Count by Distance from Store**:
     
   ![image](https://github.com/user-attachments/assets/a48b6ffb-d4ea-44ae-b254-0938ee38772a)

   - **Bike Purchase Count by Age Bracket**:
   
     ![image](https://github.com/user-attachments/assets/8b20e728-6258-45f6-91ec-b60ea2de5d53)

### 3. **Dashboard Creation**

   To bring the insights to life, I designed an interactive **Dashboard** with slicers and connections for real-time filtering. The slicers allow users to filter by categories such as **Education, Marital Status, Number of Children, Number of car ownership** and **Region**, enabling customized views for deeper insights.

![image](https://github.com/user-attachments/assets/2f6ee2de-9229-44d5-9c6d-9d6252799a31)

## 📊 How to Use

1. **Open the Excel File** and go to the **Dashboard** sheet.
2. **Explore Using Slicers** to view the data filtered by categories, offering an interactive way to explore the data.

## 📂 Data Source

The dataset is originally from Alex The Analyst, available on [GitHub](https://github.com/AlexTheAnalyst/Excel-Tutorial/blob/main/Excel%20Project%20Dataset.xlsx), and also in this repository in the `data` folder for quick reference.

## 💡 Why This Project Matters

I created this project as a practice piece to solidify my understanding of data transformation techniques and visualization skills in Excel. Working through this project allowed me to refresh my skills in Power Query, and I believe the resulting dashboard is a valuable tool for understanding customer segmentation and purchasing patterns.

## 🔧 Tools and Requirements

- **Software**: Microsoft Excel (with Power Query enabled).
- **Dataset**: Bike Buyers, structured for analysis in Power Query.

---

Thank you for exploring this project! Whether you're an Excel enthusiast or a data analytics professional, I hope this dashboard provides a clear, engaging view of how Excel can be leveraged for insightful data analysis.

