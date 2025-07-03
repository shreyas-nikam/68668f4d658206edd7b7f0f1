
# Streamlit Application Requirements Specification: Depreciation Method Analyzer

## 1. Application Overview

### 1.1 Purpose and Objectives
The "Depreciation Method Analyzer" Streamlit application provides an interactive educational tool for finance and accounting students to explore and compare various asset depreciation methods. Its primary objective is to enhance understanding of how different depreciation approaches impact reported expenses and asset book values over time.

Key learning outcomes supported by this application, referencing the provided document "Financial Statement Analysis: Understanding Income Statements":
*   **Depreciation Concept**: Understand depreciation as "the systematic allocation of costs of long-lived physical assets over their useful life" (Document, page 19, Section 6, "Issues in Expense Recognition: Depreciation and Amortization").
*   **Straight-Line Method**: Calculate annual depreciation expense using the formula:
    $$ \text{Annual Depreciation Expense} = \frac{\text{Cost} - \text{Residual value}}{\text{Estimated useful life}} $$
    (Document, page 20, Example 3).
*   **Diminishing Balance Method**: Calculate depreciation using an accelerated method that applies a constant rate to the declining net book value of the asset (Document, page 21, Example 4). The annual depreciation for a given year is calculated as $\text{Depreciation Rate} \times \text{Beginning Book Value}$, with the depreciation stopping when the asset's net book value reaches its residual value. The depreciation rate is typically derived from the straight-line rate multiplied by an acceleration factor.
*   **Sensitivity Analysis**: Analyze how "annual depreciation expense is sensitive to both the estimated useful life and to the estimated residual value" (Document, page 20, Example 3).
*   **Impact of Accelerated Methods**: Visually demonstrate that "Under accelerated depreciation methods, there is a higher depreciation expense in early years relative to the straight-line method" (Document, page 22).

### 1.2 Target Audience and Use Cases
This application is primarily targeted at finance and accounting students, educators, and professionals seeking an intuitive way to understand, visualize, and compare depreciation calculations. It serves as a practical complement to theoretical learning about long-lived assets and expense recognition.

### 1.3 Key Value Propositions
*   **Interactive Learning**: Transforms static textbook examples into dynamic, real-time calculations and visualizations.
*   **Comparative Analysis**: Enables direct comparison of depreciation methods or scenario parameters, fostering deeper analytical insights.
*   **Clarity and Simplicity**: Presents complex accounting concepts in a user-friendly and understandable format.
*   **Practical Application**: Directly relates theoretical concepts from financial statement analysis (e.g., "Implications for Financial Analysts: Expense Recognition," Document, page 23) to practical calculations.

## 2. User Interface Requirements

### 2.1 Layout and Navigation Structure
The Streamlit application will feature a two-column layout:
*   **Sidebar (Left Column)**: Dedicated to input parameters and controls.
*   **Main Display Area (Right Column)**: Displays the calculated depreciation schedule table, interactive charts, and explanatory text.
*   **Top Section**: Application title, brief overview, and key learning outcomes.

### 2.2 Input Widgets and Controls
The application will provide the following interactive input widgets:
*   **Asset Parameters**:
    *   `Asset Cost`: `st.number_input` (e.g., default: `10000`, min: `0`).
    *   `Estimated Useful Life (Years)`: `st.slider` or `st.number_input` (e.g., default: `5`, min: `1`, max: `30`).
    *   `Estimated Residual Value`: `st.number_input` (e.g., default: `1000`, min: `0`, max: `Asset Cost`). A validation check will ensure `Residual Value <= Asset Cost`.
*   **Depreciation Method Selection**:
    *   `Depreciation Method`: `st.radio` or `st.selectbox` with options:
        *   "Straight-Line Depreciation"
        *   "Diminishing Balance Depreciation"
*   **Method-Specific Parameters (Conditional Display)**:
    *   If "Diminishing Balance Depreciation" is selected:
        *   `Acceleration Factor`: `st.slider` or `st.number_input` (e.g., default: `2.0` for double-declining, min: `1.0`, max: `3.0`).
*   **Scenario Comparison**:
    *   `Compare Scenarios`: `st.checkbox` to toggle a second set of input parameters and calculations for side-by-side comparison. If checked, a second identical set of input widgets will appear in the sidebar, labeled distinctively (e.g., "Scenario 2").

### 2.3 Interactive Elements and Feedback Mechanisms
*   **Real-time Updates**: All calculations, tables, and visualizations will update automatically and instantly as users adjust any input parameters.
*   **Inline Help/Tooltips**: Contextual information, explanations of terms (e.g., "Net Book Value"), and calculation formulas will be provided via `st.info` or `st.expander` elements, particularly for the learning outcomes and document references.
*   **Error Messages**: Display clear error messages for invalid inputs (e.g., `Residual Value` exceeding `Asset Cost`, `Useful Life` being zero).

## 3. Visualization Requirements

### 3.1 Visualization Components
The main display area will feature the following visualizations:
*   **Depreciation Schedule Table**: A detailed table displaying year-by-year calculations.
    *   Columns: `Year`, `Beginning Book Value`, `Annual Depreciation Expense`, `Accumulated Depreciation`, `Ending Book Value`.
    *   If scenario comparison is enabled, the table will expand to show data for both scenarios, clearly labeled.
*   **Interactive Line Charts**:
    *   **Chart 1: Annual Depreciation Expense Over Time**: A line chart showing the `Annual Depreciation Expense` for each year of the asset's useful life. This chart will highlight the constant expense for straight-line and the declining expense for diminishing balance.
    *   **Chart 2: Net Book Value Over Time**: A line chart showing the `Ending Book Value` (carrying amount) of the asset over its useful life. This chart will demonstrate the asset's declining value on the balance sheet.
    *   If scenario comparison is enabled, both charts will overlay lines for each scenario, distinguished by color and legend.

### 3.2 Chart Types and Visualization Libraries
*   **Chart Types**: Primarily line charts (`st.line_chart`) to illustrate trends over time. Bar charts could be considered for annual expense if a more direct year-by-year comparison is desired, but line charts are sufficient for trends.
*   **Libraries**: Streamlit's built-in charting capabilities, which leverage libraries like Altair, will be used for efficiency and interactivity.

### 3.3 Interactive Visualization Features
*   **Tooltips**: On hover over chart lines or points, display precise values for `Year`, `Annual Depreciation Expense`, and `Net Book Value`.
*   **Legend**: Clearly label each line on the charts (e.g., "Straight-Line Depreciation", "Diminishing Balance Depreciation", "Scenario 1", "Scenario 2").
*   **Zoom and Pan**: Allow users to interactively explore different sections of the charts.

### 3.4 Real-time Updates and Responsiveness
*   All charts and the depreciation schedule table will automatically re-render in real-time as users modify input parameters, providing immediate visual feedback on the impact of their choices.

### 3.5 Annotation and Tooltip Specifications
*   **Annotations**: Consider optional annotations on charts to highlight specific financial implications, such as the point where accelerated depreciation expense falls below straight-line (if applicable for a combined method, or simply for comparison).
*   **Tooltips**: Detailed numerical values will appear when hovering over data points in charts and cells in tables.
*   **Explanatory Text**: Accompanying text will interpret the visualizations, explaining the observed trends and their financial implications, directly linking back to the "Learning Outcomes" and relevant sections of the "Financial Statement Analysis" document. For example, explaining why "Net Book Value" declines or why `Annual Depreciation Expense` differs between methods.
