
# Technical Specification: Income Statement Components Explorer Jupyter Notebook

## 1. Notebook Overview

### Purpose and Objectives
The primary purpose of this Jupyter Notebook is to serve as an interactive and educational tool for understanding the fundamental components, various presentation formats, and key analytical concepts related to financial income statements. It aims to provide users with a hands-on experience in constructing, modifying, and analyzing income statements.

### Target Users and Learning Goals
**Target Audience:** Finance students, junior financial analysts, small business owners, and anyone seeking a deeper understanding of financial statements.

**Learning Outcomes (referencing the provided document):**
*   **Fundamental Components:** Users will understand the core elements of an income statement, including revenues, expenses, gains, and losses, as described in the document's introduction to "Understanding Income Statements" and the section on "Components and Format of the Income Statement" (Page 2).
*   **Statement Formats:** Users will be able to differentiate between multi-step and single-step income statement formats, recognizing how subtotals like gross profit and operating profit are presented in each, consistent with the document's explanation of income statement formats (Page 7).
*   **Operating vs. Non-Operating Classification:** Users will learn to classify various revenue and expense items as operating or non-operating, and observe their impact on operating profit and net income, based on the document's learning outcome to "contrast operating and non-operating components of the income statement" and its dedicated "Non-Operating Items" section (Page 29).
*   **Expense Grouping:** Users will explore how different expense groupings (by 'nature' or by 'function') impact the income statement's appearance and analytical utility, as mentioned in the document's "Components and Format of the Income Statement" section (Page 7).
*   **Profitability Analysis:** Users will be able to calculate and interpret key profitability ratios such as gross profit margin and net profit margin (Page 43).
*   **Earnings Per Share (EPS):** Users will understand the calculation of Basic and Diluted EPS and the concepts of dilutive and antidilutive securities (Page 31, Page 39).
*   **Depreciation and Inventory Costing:** Users will grasp the impact of different depreciation methods (straight-line, declining balance) and inventory costing methods (FIFO, Weighted-Average) on reported expenses and net income (Page 16, Page 20).

### Expected Outcomes and Value
Upon completion, users will:
*   Possess a strong conceptual and practical understanding of income statement construction.
*   Be proficient in identifying and categorizing various income and expense items.
*   Be able to analyze the impact of different accounting choices (formats, expense grouping, depreciation, inventory costing, EPS calculation) on reported financial performance.
*   Develop a foundational skill set for financial analysis, bridging theoretical knowledge from the document with practical application.

## 2. Notebook Structure and Flow

The notebook will be logically divided into modular sections, each focusing on a specific aspect of the income statement. Markdown cells will provide theoretical background and explanations, while code cells will facilitate interactive data input, calculations, and visualizations.

### Suggested Number and Order of Sections

1.  **Title and Introduction:**
    *   **Markdown:** Notebook title, brief overview, learning outcomes, and how the notebook relates to the "Understanding Income Statements" document.
2.  **Section 1: Income Statement Fundamentals**
    *   **Markdown:** Explanation of the basic income statement equation ($Revenue - Expenses = Net\\ Income$), purpose, and periodicity (Page 2). Definition of Revenue (Page 3, Page 9) and Expenses (Page 6, Page 14).
    *   **Code:** Simple fixed data to illustrate initial income statement structure.
3.  **Section 2: Income Statement Formats (Single-Step vs. Multi-Step)**
    *   **Markdown:** Detailed explanation of single-step and multi-step formats, highlighting key subtotals like Gross Profit and Operating Profit (Page 7).
    *   **Code & Interactive Elements:**
        *   User inputs for core revenue and expense items (Sales, COGS, Operating Expenses, Non-Operating Income/Expenses).
        *   Toggle/Dropdown to switch between "Single-Step" and "Multi-Step" presentation.
        *   Dynamic display of the income statement reflecting the chosen format.
        *   Real-time calculation of $Gross\\ Profit = Revenue - Cost\\ of\\ Goods\\ Sold$ and $Operating\\ Profit = Gross\\ Profit - Operating\\ Expenses$.
4.  **Section 3: Expense Grouping (By Nature vs. By Function)**
    *   **Markdown:** Explanation of grouping expenses by 'nature' (e.g., depreciation for all assets) or 'function' (e.g., cost of sales, administrative expenses) as discussed in the document (Page 7).
    *   **Code & Interactive Elements:**
        *   Example data showing expenses classified both ways.
        *   Toggle/Dropdown to switch between 'Nature' and 'Function' grouping for a set of sample expenses.
        *   Display of how the income statement presentation changes.
5.  **Section 4: Operating vs. Non-Operating Items**
    *   **Markdown:** Definition and distinction between operating and non-operating income/expense items (e.g., finance costs, finance income, gains/losses from asset disposal) (Page 29). Explanation of their significance for analysis.
    *   **Code & Interactive Elements:**
        *   Input fields for specific non-operating items (e.g., Finance Costs, Finance Income, Share of Associates' Profit/Loss).
        *   Clear separation and highlighting of "Operating Profit" and "Non-Operating Items" in the displayed statement.
        *   Calculations reflecting their impact on *Profit before tax*.
6.  **Section 5: Key Profitability Ratios**
    *   **Markdown:** Introduction to profitability ratios, specifically Net Profit Margin ($Net\\ Profit\\ Margin = \frac{Net\\ Income}{Revenue}$) and Gross Profit Margin ($Gross\\ Profit\\ Margin = \frac{Gross\\ Profit}{Revenue}$) (Page 43). Discussion of their interpretation.
    *   **Code:** Calculation and display of these ratios based on the constructed income statement.
7.  **Section 6: Expense Recognition Applications (Deep Dive)**
    *   **Markdown:**
        *   **Inventory Costing:** Explanation of FIFO and Weighted Average Cost methods for Cost of Goods Sold (COGS) (Page 16).
        *   **Depreciation:** Explanation of Straight-Line and Double Declining Balance methods (Page 20, Page 21).
        *   **Doubtful Accounts & Warranties:** Brief theoretical overview of matching principle (Page 18).
    *   **Code & Interactive Elements:**
        *   **Inventory:** Example data set for inventory purchases and sales. Dropdown to select FIFO or Weighted-Average method. Display of calculated COGS and Ending Inventory.
        *   **Depreciation:** Inputs for Asset Cost, Useful Life, Residual Value. Dropdown to select Straight-Line or Double Declining Balance. Calculation and display of annual depreciation expense over the asset's life.
8.  **Section 7: Earnings Per Share (EPS)**
    *   **Markdown:** Explanation of Basic EPS and Diluted EPS. Concepts of simple vs. complex capital structures. Formulas for Basic EPS (Page 31), Diluted EPS with convertible preferred stock (Page 34), convertible debt (Page 35), and stock options (Treasury Stock Method) (Page 37). Discussion of dilutive vs. antidilutive securities (Page 39).
    *   **Code & Interactive Elements:**
        *   Inputs for Net Income, Preferred Dividends, Weighted Average Shares Outstanding.
        *   Optional inputs for convertible preferred shares (conversion ratio, dividends), convertible debt (interest, conversion ratio, tax rate), and stock options (exercise price, average market price).
        *   Calculations and display of Basic EPS and Diluted EPS.
        *   Logic to identify if a security is antidilutive and exclude it from diluted EPS calculation as per accounting standards (Page 39).
9.  **Section 8: Comprehensive Income (Brief)**
    *   **Markdown:** High-level overview of Comprehensive Income, including Net Income and Other Comprehensive Income (OCI) (Page 45).
    *   **Code:** Simple example calculation for comprehensive income.
10. **Conclusion and Further Exploration:**
    *   **Markdown:** Summary of key takeaways, suggestions for further learning, and open-ended questions for users to consider.

### Where to Place Markdown Explanations vs. Code Blocks
*   **Markdown:** Precedes each major concept or sub-section. It introduces the topic, defines terms, provides theoretical background, and explains formulas. It sets the context for the code that follows.
*   **Code Blocks:** Follows the relevant markdown explanation. It implements the concepts discussed, handles user inputs, performs calculations, and generates outputs (tables, charts). Comments within code blocks will explain specific logic.

### Logical Progression of Concepts and Tasks
The notebook will follow a "building block" approach:
1.  **Foundation:** Start with the very basics of income statements.
2.  **Core Structure:** Introduce the common formats.
3.  **Component Deep Dive:** Break down different types of expenses and their presentation.
4.  **Key Metrics:** Calculate and interpret primary profitability ratios.
5.  **Accounting Choices Impact:** Demonstrate how different accounting methods (inventory, depreciation) alter the figures.
6.  **Advanced Metrics:** Explain and calculate Earnings Per Share, and briefly touch on Comprehensive Income.
This flow ensures that users build knowledge incrementally, reinforcing understanding with practical examples and interactive exercises at each step.

## 3. Mathematical and Theoretical Foundations

This section details the key mathematical formulas and theoretical concepts to be explained and implemented, adhering strictly to LaTeX formatting.

### Core Income Statement Equation
The fundamental equation is:

$$
 Net\\ Income = Revenue - Expenses 
$$

This equation represents the profitability of a business over a period (Page 2).

### Profitability Subtotals
*   **Gross Profit:**
    $Gross\\ Profit = Revenue - Cost\\ of\\ Goods\\ Sold$ (Page 3, Page 7)
    *   *Definition:* The profit a company makes after deducting the costs associated with making and selling its products, or the costs associated with providing its services (Page 7).
*   **Operating Profit (or Operating Income):**
    $Operating\\ Profit = Gross\\ Profit - Operating\\ Expenses$ (Page 7)
    *   *Definition:* Reflects a company's profits on its business activities before deducting taxes and, for non-financial companies, before deducting interest expense (Page 7).

### Key Profitability Ratios
*   **Net Profit Margin:**
    
$$
 Net\\ Profit\\ Margin = \frac{Net\\ Income}{Revenue} 
$$

    *   *Definition:* Measures the amount of income generated for each dollar of revenue (Page 43).
*   **Gross Profit Margin:**
    
$$
 Gross\\ Profit\\ Margin = \frac{Gross\\ Profit}{Revenue} 
$$

    *   *Definition:* Measures the amount of gross profit generated for each dollar of revenue (Page 43).

### Depreciation Methods
*   **Straight-Line Depreciation:**
    
$$
 Annual\\ Depreciation\\ Expense = \frac{Cost - Residual\\ Value}{Useful\\ Life} 
$$

    *   *Definition:* Allocates the depreciable cost of an asset evenly over its estimated useful life (Page 20).
*   **Double Declining Balance Depreciation:**
    *   First, calculate the Straight-Line Depreciation Rate: $Straight-Line\\ Rate = \frac{1}{Useful\\ Life}$
    *   Then, the Double Declining Balance Rate: $DDB\\ Rate = Straight-Line\\ Rate \times 2$
    *   Annual Depreciation Expense: $Depreciation = Net\\ Book\\ Value \times DDB\\ Rate$
    *   *Note:* Depreciation stops when the asset's book value equals its residual value.
    *   *Definition:* An accelerated depreciation method that applies a constant rate (double the straight-line rate) to the asset's declining net book value each period, resulting in higher depreciation in earlier years (Page 21).

### Earnings Per Share (EPS)
*   **Basic EPS:**
    
$$
 Basic\\ EPS = \frac{Net\\ Income - Preferred\\ Dividends}{Weighted\\ Average\\ Number\\ of\\ Shares\\ Outstanding} 
$$

    *   *Definition:* The amount of income available to common shareholders, divided by the weighted average number of common shares outstanding (Page 31).
*   **Diluted EPS (If-Converted Method - Preferred Stock):**
    
$$
 Diluted\\ EPS = \frac{Net\\ Income}{Weighted\\ Average\\ Number\\ of\\ Shares\\ Outstanding + New\\ Common\\ Shares\\ from\\ Conversion} 
$$

    *   *Definition:* Calculates EPS assuming all convertible preferred shares were converted at the beginning of the period, increasing common shares and eliminating preferred dividends (Page 34).
*   **Diluted EPS (If-Converted Method - Convertible Debt):**
    
$$
 Diluted\\ EPS = \frac{Net\\ Income + After-tax\\ Interest\\ on\\ Convertible\\ Debt - Preferred\\ Dividends}{Weighted\\ Average\\ Number\\ of\\ Shares\\ Outstanding + Additional\\ Common\\ Shares\\ from\\ Conversion} 
$$

    *   *Definition:* Calculates EPS assuming convertible debt was converted, increasing common shares and saving after-tax interest expense (Page 35).
    *   $After-tax\\ Interest\\ on\\ Convertible\\ Debt = Interest\\ Expense \times (1 - Tax\\ Rate)$
*   **Diluted EPS (Treasury Stock Method - Options/Warrants):**
    
$$
 Diluted\\ EPS = \frac{Net\\ Income - Preferred\\ Dividends}{Weighted\\ Average\\ Number\\ of\\ Shares\\ Outstanding + Incremental\\ Shares\\ from\\ Options} 
$$

    Where:
    *   $Shares\\ from\\ Exercise = Number\\ of\\ Options \times Shares\\ per\\ Option$
    *   $Proceeds\\ from\\ Exercise = Shares\\ from\\ Exercise \times Exercise\\ Price$
    *   $Shares\\ Repurchased = \frac{Proceeds\\ from\\ Exercise}{Average\\ Market\\ Price}$
    *   $Incremental\\ Shares\\ from\\ Options = Shares\\ from\\ Exercise - Shares\\ Repurchased$
    *   *Definition:* Calculates EPS assuming options/warrants are exercised and proceeds are used to repurchase shares from the market, increasing shares outstanding by the net incremental amount (Page 37).
*   **Antidilutive Securities:** Securities whose conversion or exercise would result in an EPS higher than the company's basic EPS. These are *not* included in the diluted EPS calculation (Page 39).

### Comprehensive Income
*   **Comprehensive Income:**
    $Comprehensive\\ Income = Net\\ Income + Other\\ Comprehensive\\ Income$ (Page 45)
    *   *Definition:* The change in equity during a period from transactions and other events and circumstances from non-owner sources (Page 45).
*   **Other Comprehensive Income (OCI):** Includes items of income and expense not recognized in net income (e.g., unrealized gains/losses on certain investments, foreign currency translation adjustments) (Page 45).

## 4. Code Requirements

The code will focus on data generation, calculation logic, and preparing data for visualization.

### Algorithms or Methods to be Implemented
1.  **Synthetic Data Generation:**
    *   Functions to generate a baseline set of income statement line items (e.g., `generate_income_statement_data(revenue, cogs_rate, op_exp_rate, non_op_inc_rate, non_op_exp_rate, tax_rate)`).
    *   Flexibility to add "noise" or slight variations for multiple periods to simulate trends.
2.  **Income Statement Format Logic:**
    *   Function (`generate_single_step_is`) to construct a single-step income statement format: all revenues grouped, all expenses grouped, then net income.
    *   Function (`generate_multi_step_is`) to construct a multi-step income statement format: Gross Profit, Operating Profit, Profit Before Tax, Net Income.
3.  **Expense Grouping Logic:**
    *   Functions to transform raw expense data into 'by nature' or 'by function' groupings. This might involve mapping detailed expense items to broader categories.
    *   Example: Raw expenses: `Salaries`, `Depreciation`, `Rent`, `Marketing`.
        *   By Nature: `Depreciation`, `Employee Benefits`, `Rent Expense`, `Advertising Expense`.
        *   By Function: `Cost of Sales` (includes some salaries/depreciation), `Administrative Expenses` (includes other salaries/depreciation/rent), `Marketing Expenses`.
4.  **Operating vs. Non-Operating Segregation:**
    *   Logic to clearly identify and separate operating expenses/income from non-operating expenses/income based on predefined categories.
5.  **Financial Ratio Calculations:**
    *   Functions for `gross_profit_margin()`, `net_profit_margin()`.
6.  **Inventory Costing Logic:**
    *   Function (`calculate_fifo_cogs(purchases, sales_units)`) to implement First-In, First-Out (FIFO).
    *   Function (`calculate_weighted_average_cogs(purchases, sales_units)`) to implement Weighted Average Cost.
7.  **Depreciation Calculation Logic:**
    *   Function (`calculate_straight_line_depreciation(cost, residual, useful_life)`)
    *   Function (`calculate_ddb_depreciation(cost, residual, useful_life)`) to calculate depreciation for each year, ensuring it doesn't fall below residual value.
8.  **EPS Calculation Logic:**
    *   Function (`calculate_basic_eps(net_income, preferred_dividends, shares_outstanding)`)
    *   Function (`calculate_diluted_eps(net_income, preferred_dividends, shares_outstanding, dilutive_securities, tax_rate)`) that incorporates the if-converted method for preferred stock and convertible debt, and the treasury stock method for options/warrants. Includes logic for antidilution.

### Input/Output Expectations
*   **Input Mechanisms:** Python variables set in code cells, or simple input functions using `input()` for basic demonstrations. For a more interactive feel within Jupyter, text fields and dropdowns can be simulated with variable assignments and comments guiding the user to change values. (No `ipywidgets` unless explicitly requested, as the prompt specifies "if any" for interactive elements and avoids deployment specifics).
    *   **Financial Figures:** `sales`, `cogs`, `admin_exp`, `marketing_exp`, `rd_exp`, `finance_cost`, `finance_income`, `tax_rate`, `net_income`, `preferred_dividends`, `common_shares_outstanding`, `option_exercise_price`, `stock_market_price`, `asset_cost`, `asset_useful_life`, `asset_residual_value`.
    *   **Categorical Choices:** `statement_format` (single-step/multi-step), `expense_grouping` (nature/function), `depreciation_method` (straight-line/ddb), `inventory_method` (fifo/weighted_average).
*   **Output Presentation:**
    *   Formatted `pandas.DataFrame` objects representing income statements.
    *   Printed results for ratio calculations, EPS figures.
    *   `matplotlib` or `seaborn` plots embedded directly in the notebook output.

### Expected Libraries and How They Will Be Used
*   **`pandas`:** For creating and manipulating tabular data (income statements, inventory schedules, depreciation schedules). Critical for structured data presentation.
*   **`numpy`:** For numerical operations, especially for calculations involving rates, percentages, and financial formulas.
*   **`matplotlib.pyplot`:** For generating static visualizations like bar charts (expense breakdown, operating vs non-operating), line charts (depreciation over time), and comparison plots.
*   **`seaborn` (optional, for enhanced aesthetics):** Can be used on top of `matplotlib` for more visually appealing statistical plots.

## 5. Visualization and Output Expectations

This section details the expected visual and tabular outputs, focusing on clarity and aiding comprehension.

### Charts, Tables, Plots that Should be Generated
1.  **Formatted Income Statements (Tables):**
    *   A `pandas.DataFrame` displayed as a clean table, showcasing the income statement in both **single-step** and **multi-step** formats, side-by-side or toggled, based on user selection.
    *   Similar tables to demonstrate expenses grouped by **nature** vs. **function**.
    *   Tables clearly distinguishing **operating** from **non-operating** items.
2.  **Comparative Bar Charts:**
    *   **Operating vs. Non-Operating Components:** A bar chart comparing the magnitude of "Operating Profit" versus the net effect of "Non-Operating Items" on Profit Before Tax.
    *   **Expense Breakdown:** A bar chart or pie chart illustrating the proportion of different expense categories (e.g., COGS, Admin, Marketing, R&D) relative to total revenue or total expenses, adaptable for 'nature' vs. 'function' views.
    *   **Profitability Ratios Over Time (Simulated):** If simulating multiple periods, line charts showing trends in Gross Profit Margin and Net Profit Margin.
3.  **Depreciation Schedules (Table & Line Plot):**
    *   A table showing annual depreciation expense and net book value for each year of the asset's life under both **straight-line** and **double declining balance** methods.
    *   A line plot comparing the accumulated depreciation or net book value over time for the different methods.
4.  **EPS Comparison (Table & Bar Chart):**
    *   A table presenting `Basic EPS` and `Diluted EPS` figures, alongside the components of their numerator and denominator.
    *   A simple bar chart comparing the Basic EPS and Diluted EPS values to visually emphasize any dilution.
5.  **Inventory Costing Comparison (Table):**
    *   A table demonstrating the calculation of `Cost of Goods Sold` and `Ending Inventory` under the **FIFO** and **Weighted Average Cost** methods given a series of purchases and sales.

### Tools/Libraries Used for Visualization
*   **`pandas`:** For displaying structured data in clear, readable tables.
*   **`matplotlib.pyplot`:** For all charting needs (bar charts, line plots). Will be used to create clear, concise visualizations.
*   **`seaborn`:** (Optional but recommended) For enhanced aesthetic appeal and statistical plotting capabilities to make charts more engaging and professional.

### Optional Interactivity via Widgets or Plots
While avoiding explicit platform-specific widgets like Streamlit, the "interactive elements" can be simulated through:
*   **Pre-defined scenarios:** Users can uncomment/modify variables in code cells to quickly switch between scenarios (e.g., different revenue figures, expense structures, format choices).
*   **Clear instructions:** Markdown cells will guide users on how to modify input parameters (e.g., "Change the value of `revenue = 1000000` to `revenue = 1200000` in the cell below and re-run to see the impact.").
*   **Dropdowns (simulated):** A code cell can have a variable `selected_format = "Multi-Step"` with comments like `# Options: "Single-Step", "Multi-Step"`, prompting users to manually change and re-run.

## 6. Additional Notes or Instructions

### Assumptions
*   The notebook assumes a basic understanding of Python programming concepts (variables, functions, data structures like lists and dictionaries).
*   All financial figures used will be synthetic, generated within the notebook, to maintain a controlled environment and focus on the accounting principles.
*   Simplifications may be made for certain complex accounting treatments (e.g., deferred taxes, detailed consolidation rules) to prioritize pedagogical clarity on core income statement concepts.
*   The notebook will operate in a standard Jupyter environment (Jupyter Notebook or JupyterLab).

### Constraints
*   **No Deployment Steps:** The specification explicitly avoids any instructions or references related to deploying the application (e.g., to Streamlit, Dash, etc.). The focus is purely on the self-contained Jupyter Notebook experience.
*   **No External Data Sources:** All data used will be synthetically generated or hardcoded within the notebook. No external CSVs, databases, or APIs will be accessed.
*   **Static Outputs Primarily:** While interaction is simulated via variable changes and re-running cells, dynamic, real-time widgets (like `ipywidgets` that require a live kernel for continuous updates) are considered optional and will not be the primary mode of interaction unless explicitly desired and implemented carefully to avoid exceeding the "no deployment steps" constraint. Simple sliders/dropdowns can be included as conceptual interactive elements if implemented purely within the notebook's execution flow.

### Customization Instructions
*   Users will be encouraged to modify the input values in designated code cells to experiment with different financial scenarios.
*   Suggestions will be provided for users to extend the notebook, such as adding new expense categories, implementing other depreciation methods (e.g., units of production), or incorporating more complex EPS scenarios.
*   Guidance on how to modify visualization parameters (e.g., chart types, colors, labels) using `matplotlib` will be included.

### Relation of the lab to the concept
This notebook directly bridges the theoretical concepts presented in the "Understanding Income Statements" document with practical, hands-on application. For example:
*   The **Dynamic Statement Builder** feature directly addresses the document's learning outcome to "describe the components of the income statement and alternative presentation formats of that statement" (Page 1), allowing users to visually construct and switch between multi-step and single-step formats (Page 7).
*   The **Operating vs. Non-Operating Breakdown** reinforces the document's directive to "contrast operating and non-operating components of the income statement" (Page 1) and details from the "Non-Operating Items" section (Page 29).
*   The **Interactive Components Toggle** for expense grouping by 'nature' or 'function' directly demonstrates a concept highlighted in the "Components and Format of the Income Statement" section (Page 7), providing a visual understanding of how expense presentation impacts clarity.
*   The **Real-time Calculations** for gross profit (Page 3, Page 7), operating profit (Page 7), and net income directly apply the formulas and definitions from the document, allowing users to see the immediate effects of input changes.
*   The detailed sections on **Inventory Costing**, **Depreciation**, and **Earnings Per Share** provide practical implementations of the theoretical explanations and examples found throughout the document (e.g., Example 1 & 2 for Inventory on Page 15-16, Example 3 & 4 for Depreciation on Page 20-21, and Examples 6-13 for EPS on Page 32-39). This reinforces the understanding of how accounting choices impact reported financial figures.
By manipulating these elements, users gain a deeper, more intuitive understanding of income statement analysis and the implications of various accounting policies, beyond just reading the text.


### Appendix Code

```code
Revenue
Cost of sales
Gross profit
Distribution expenses
Sales and marketing expenses
Administrative expenses
Other operating income/(expenses)
Restructuring
Business and asset disposal
Acquisition costs business combinations
Impairment of assets
Judicial settlement
Profit from operations
Finance cost
Finance income
Net finance income/(cost)
Share of result of associates and joint ventures
Profit before tax
Income tax expense
Profit from continuing operations
Profit from discontinued operations
Profit of the year
Profit from continuing operations attributable to:
Equity holders of AB InBev
Non-controlling interest
Profit of the year attributable to:
Equity holders of AB InBev
Non-controlling interest

```
Reference: Exhibit 1: Anheuser-Busch InBev SA/NV Consolidated Income Statement (in Millions of US Dollars) [Excerpt] (Page 3-4)

```
Sales
Excise taxes
Net sales
Cost of goods sold
Gross profit
Marketing, general and administrative expenses
Special items, net
Equity Income in MillerCoors
Operating income (loss)
Other income (expense), net
Interest expense
Interest income
Other income (expense), net
Total other income (expense), net
Income (loss) from continuing operations before income taxes
Income tax benefit (expense)
Net income (loss) from continuing operations
Income (loss) from discontinued operations, net of tax
Net income (loss) including noncontrolling interests
Net (income) loss attributable to noncontrolling interests
Net income (loss) attributable to Molson Coors Brewing Company
```
Reference: Exhibit 2: Molson Coors Brewing Company Consolidated Statement of Operations (in Millions of US Dollars) [Excerpt] (Page 4-5)

```
Sales
Cost of goods sold
Selling expense
General and administrative expense
Research and development expense
Other income (expense)
Recurring operating income
Other operating income (expense)
Operating income
Interest income on cash equivalents and short-term investments
Interest expense
Cost of net debt
Other financial income
Other financial expense
Income before tax
Income tax expense
Net income from fully consolidated companies
Share of profit of associates
Net income
Net income – Group share
Net income - Non-controlling interests
```
Reference: Exhibit 3: Groupe Danone Consolidated Income Statement (in Millions of Euros) [Excerpt] (Page 5)

```
Revenues
Costs of services (exclusive of depreciation and amortization)
Selling, general and administrative expenses
Depreciation and amortization
GNU goodwill impairment
Income from operations
```
Reference: Exhibit 4: CRA International Inc. Consolidated Statements of Operations (Excerpt) (in Thousands of Dollars) (Page 8)

```
Builder Co. has incurred 60% of the total expected costs ($420,000/$700,000) and will thus recognize $600,000 (60% × $1 million) in revenue for the first year.
```
Reference: Exhibit 5, Part 2 (ref. Example 8) (Page 12)

```
Builder's total revenue on the transaction (transaction price) is now $1.35 million ($1 million original plus the $150,000 new consideration plus $200,000 for the completion bonus). Builder Co's progress toward completion is now 51.2% ($420,000 costs incurred divided by total expected costs of $820,000). Based on the changes in the contract, the amount of additional revenue to be recognized is $91,200, calculated as (51.2% × $1.35 million) minus the $600,000 already recognized.
```
Reference: Exhibit 5, Part 4 (ref. Example 8) (Page 12-13)

```
Inventory Purchases
First quarter	2,000 units at $40 per unit
Second quarter	1,500 units at $41 per unit
Third quarter	2,200 units at $43 per unit
Fourth quarter	1,900 units at $45 per unit
Total		7,600 units at a total cost of $321,600

Cost of Goods Sold
From the first quarter	2,000 units at $40 per unit = $80,000
From the second quarter	1,500 units at $41 per unit = $61,500
From the third quarter	2,100 units at $43 per unit = $90,300
Total cost of goods sold	$231,800

Cost of Goods Remaining in Inventory
From the third quarter	100 units at $43 per unit = $4,300
From the fourth quarter	1,900 units at $45 per unit = $85,500
Total remaining (or ending) inventory cost $89,800

To confirm that total costs are accounted for: $231,800 + $89,800 = $321,600.
```
Reference: EXAMPLE 1: The Matching of Inventory Costs with Revenues (Page 15-16)

```
Revenue          $280,000
Cost of goods sold 231,800
Gross profit     $48,200
```
Reference: EXAMPLE 1: The Matching of Inventory Costs with Revenues (Page 16)

```
For KDL, the weighted average cost per unit would be
$321,600/7,600 units = $42.3158 per unit
Cost of goods sold using the weighted average cost method would be
5,600 units at $42.3158 = $236,968
```
Reference: EXAMPLE 2: Alternative Inventory Costing Methods (Page 16)

```
Ending inventory 2,000 units at $40 per unit = $80,000
Total costs of $321,600 less $80,000 remaining in ending inventory = $241,600
Alternatively, the cost of the last 5,600 units purchased is allocated to cost of goods sold under LIFO:
1,900 units at $45 per unit + 2,200 units at $43 per unit + 1,500 units at $41 per unit = $241,600
```
Reference: EXAMPLE 2: Alternative Inventory Costing Methods (Page 17)

```
Method               Description                                                Cost of Goods Sold When Prices Are Rising, Relative to Other Two Methods    Ending Inventory When Prices Are Rising, Relative to Other Two Methods
FIFO (first in, first out)   Costs of the earliest items purchased flow to cost of goods sold first   Lowest                                                      Highest
LIFO (last in, first out)    Costs of the most recent items purchased flow to cost of goods sold first   Highest*                                                    Lowest*
Weighted average cost      Averages total costs over total units available        Middle                                                      Middle
```
Reference: Exhibit 6: Summary Table on Inventory Costing Methods (Page 17-18)

```
Cost - Residual value
Estimated useful life

Assume the cost of an asset is $10,000. If, for example, the residual value of the asset is estimated to be $0 and its useful life is estimated to be 5 years, the annual depreciation expense under the straight-line method would be ($10,000 - $0)/5 years = $2,000. In contrast, holding the estimated useful life of the asset constant at 5 years but increasing the estimated residual value of the asset to $4,000 would result in annual depreciation expense of only $1,200 [calculated as ($10,000 – $4,000)/5 years]. Alternatively, holding the estimated useful life of the asset to 10 years would result in annual depreciation expense of only $1,000 [calculated as ($10,000 – $0)/10 years].
```
Reference: EXAMPLE 3: Sensitivity of Annual Depreciation Expense to Varying Estimates of Useful Life and Residual Value (Page 20)

```
Estimated
Useful Life (Years)
Estimated Residual Value
         0     1,000  2,000  3,000  4,000  5,000
2        5,000  4,500  4,000  3,500  3,000  2,500
4        2,500  2,250  2,000  1,750  1,500  1,250
5        2,000  1,800  1,600  1,400  1,200  1,000
8        1,250  1,125  1,000  875    750    625
10       1,000  900    800    700    600    500
```
Reference: Exhibit 7: Annual Depreciation Expense (in Dollars) (Page 20-21)

```
Assume the cost of computer equipment was $11,000, the estimated residual value is $1,000, and the estimated useful life is five years. Under the diminishing or declining balance method, the first step is to determine the straight-line rate, the rate at which the asset would be depreciated under the straight-line method. This rate is measured as 100 percent divided by the useful life or 20 percent for a five-year useful life. Under the straight-line method, 1/5 or 20 percent of the depreciable cost of the asset (here, $11,000 – $1,000 = $10,000) would be expensed each year for five years: The depreciation expense would be $2,000 per year.
The next step is to determine an acceleration factor that approximates the pattern of the asset's wear. Common acceleration factors are 150 percent and 200 percent. The latter is known as double declining balance depreciation because it depreciates the asset at double the straight-line rate. Using the 200 percent acceleration factor, the diminishing balance rate would be 40 percent (20 percent × 2.0). This rate is then applied to the remaining undepreciated balance of the asset each period (known as the net book value).
At the beginning of the first year, the net book value is $11,000. Depreciation expense for the first full year of use of the asset would be 40 percent of $11,000, or $4,400.
```
Reference: EXAMPLE 4: An Illustration of Diminishing Balance Depreciation (Page 21)

```
Asset cost                  $11,000
Less: Accumulated depreciation (4,400)
Net book value              $6,600

For the second full year, depreciation expense would be $6,600 × 40 percent, or $2,640.
```
Reference: EXAMPLE 4: An Illustration of Diminishing Balance Depreciation (Page 21)

```
Asset cost                  $11,000
Less: Accumulated depreciation (7,040)
Net book value              $3,960

For the third full year, depreciation would be $3,960 × 40 percent, or $1,584.
```
Reference: EXAMPLE 4: An Illustration of Diminishing Balance Depreciation (Page 22)

```
Asset cost                  $11,000
Less: Accumulated depreciation (8,624)
Net book value              $2,376

For the fourth full year, depreciation would be $2,376 × 40 percent, or $950.
```
Reference: EXAMPLE 4: An Illustration of Diminishing Balance Depreciation (Page 22)

```
Asset cost                  $11,000
Less: Accumulated depreciation (9,574)
Net book value              $1,426

For the fifth year, if deprecation were determined as in previous years, it would amount to $570 ($1,426 × 40 percent). However, this would result in a remaining net book value of the asset below its estimated residual value of $1,000. So, instead, only $426 would be depreciated, leaving a $1,000 net book value at the end of the fifth year.
```
Reference: EXAMPLE 4: An Illustration of Diminishing Balance Depreciation (Page 22)

```
Asset cost                  $11,000
Less: Accumulated depreciation (10,000)
Net book value              $1,000
```
Reference: EXAMPLE 4: An Illustration of Diminishing Balance Depreciation (Page 22)

```
(in € millions)                                          Related income
                                                         (expense)
Capital gain on disposal of Stonyfield                         628
Compensation received following the decision of the Singapore arbi-  105
tration court in the Fonterra case
Territorial risks, mainly in certain countries in the ALMA region     (148)
Costs associated with the integration of WhiteWave                (118)
Impairment of several intangible assets in Waters and Specialized  (115)
Nutrition Reporting entities
```
Reference: Exhibit 8: Highlighting Infrequent Nature of Items—Excerpt from Groupe Danone footnotes to its 2017 financial statements (Page 26)

```
(In $ millions, except per share   As        New Revenue    As
amounts)                          Previously  Standard       Restated
                                  Reported    Adjustment

Income Statements
Year Ended June 30, 2017
Revenue                           89,950      6,621          96,571
Provision for income taxes        1,945       2,467          4,412
Net income                        21,204      4,285          25,489
Diluted earnings per share        2.71        0.54           3.25

Year Ended June 30, 2016
Revenue                           85,320      5,834          91,154
Provision for income taxes        2,953       2,147          5,100
Net income                        16,798      3,741          20,539
Diluted earnings per share        2.1         0.46           2.56
```
Reference: EXAMPLE 5: Microsoft Corporation Excerpt from Footnotes to the Financial Statements (Page 27)

```
Microsoft's results appear better under the new revenue recognition standard. Revenues and income are higher under the new standard. The net profit margin is higher under the new standard. For 2017, the net profit margin is 26.4% (= 25,489/96,571) under the new standard versus 23.6% (= 21,204/89,950) under the old standard. Reported revenue grew faster under the new standard. Revenue growth under the new standard was 5.9% [= (96,571/91,154) – 1] compared to 5.4% [= (89,950/85,320) – 1)] under the old standard.
```
Reference: EXAMPLE 5, Solution (Page 28)

```
Basic EPS = Net income - Preferred dividends
            -------------------------------------
            Weighted average number of shares outstanding
```
Reference: Basic EPS formula (Page 31)

```
Basic earnings per share
Diluted earnings per share
Basic earnings per share from continuing operations
Diluted earnings per share from continuing operations
```
Reference: Exhibit 10: AB InBev's Earnings Per Share (Page 31)

```
Shopalot's basic EPS is $1.30 ($1,950,000 divided by 1,500,000 shares).
```
Reference: EXAMPLE 6: A Basic EPS Calculation (1), Solution (Page 32)

```
Shares outstanding on 1 January 2018      1,000,000
Shares issued on 1 April 2018              200,000
Shares repurchased (treasury shares) on 1 October 2018 (100,000)
Shares outstanding on 31 December 2018    1,100,000

The weighted average number of shares outstanding is determined by the length of time each quantity of shares was outstanding:
1,000,000 x (3 months/12 months) = 250,000
1,200,000 × (6 months/12 months) = 600,000
1,100,000 x (3 months/12 months) = 275,000
Weighted average number of shares outstanding = 1,125,000
```
Reference: EXAMPLE 7: A Basic EPS Calculation (2), Solution to 1 (Page 32)

```
Basic EPS = (Net income – Preferred dividends)/Weighted average number of shares = ($2,500,000 – $200,000)/1,125,000 = $2.04
```
Reference: EXAMPLE 7: A Basic EPS Calculation (2), Solution to 2 (Page 33)

```
For EPS calculation purposes, a stock split is treated as if it occurred at the beginning of the period. The weighted average number of shares would, therefore, be 2,250,000, and the basic EPS would be $1.02 [= ($2,500,000 – $200,000)/2,250,000].
```
Reference: EXAMPLE 8: A Basic EPS Calculation (3), Solution (Page 33)

```
Diluted EPS = (Net income)
              -----------------------------------------------------
              (Weighted average number of shares
              outstanding + New common shares that
              would have been issued at conversion)
```
Reference: Diluted EPS formula (Page 34)

```
If the 20,000 shares of convertible preferred had each converted into 5 shares of the company's common stock, the company would have had an additional 100,000 shares of common stock (5 shares of common for each of the 20,000 shares of preferred). If the conversion had taken place, the company would not have paid preferred dividends of $200,000 ($10 per share for each of the 20,000 shares of preferred). As shown in Exhibit 11, the company's basic EPS was $3.10 and its diluted EPS was $2.92.
```
Reference: EXAMPLE 9: A Diluted EPS Calculation Using the If-Converted Method for Preferred Stock, Solution (Page 34)

```
              Basic EPS    Diluted EPS Using
                           If-Converted Method
Net income    $1,750,000   $1,750,000
Preferred dividend -200,000     0
Numerator     $1,550,000   $1,750,000
Weighted average number of shares
outstanding   500,000      500,000
Additional shares issued if preferred
converted     0            100,000
Denominator   500,000      600,000
EPS           $3.10        $2.92
```
Reference: Exhibit 11: Calculation of Diluted EPS for Bright-Warm Utility Company Using the If-Converted Method: Case of Preferred Stock (Page 34-35)

```
Diluted EPS = (Net income + After-tax interest on
             convertible debt - Preferred dividends)
             -----------------------------------------------------
             (Weighted average number of shares
             outstanding + Additional common
             shares that would have been
             issued at conversion)
```
Reference: Diluted EPS formula (Convertible Debt) (Page 35)

```
If the debt securities had been converted, the debt securities would no longer be outstanding and instead, an additional 10,000 shares of common stock would be outstanding. Also, if the debt securities had been converted, the company would not have paid interest of $3,000 on the convertible debt, so net income available to common shareholders would have increased by $2,100 [= $3,000(1 – 0.30)] on an after-tax basis.
```
Reference: EXAMPLE 10: A Diluted EPS Calculation Using the If-Converted Method for Convertible Debt, Solution (Page 35)

```
                       Basic EPS    Diluted EPS Using
                                  If-Converted Method
Net income             $750,000     $750,000
After-tax cost of interest           2,100
Numerator              $750,000     $752,100
Weighted average number of shares
outstanding            690,000      690,000
If converted           0            10,000
Denominator            690,000      700,000
EPS                    $1.09        $1.07
```
Reference: Exhibit 12: Calculation of Diluted EPS for Oppnox Company Using the If-Converted Method: Case of a Convertible Bond (Page 36)

```
Diluted EPS = (Net income - Preferred dividends)
             --------------------------------------------------------------------------------------
             [Weighted average number of shares
             outstanding + (New shares that would
             have been issued at option exercise -
             Shares that could have been purchased
             with cash received upon exercise) x
             (Proportion of year during which the
             financial instruments were outstanding)]
```
Reference: Diluted EPS formula (Options) (Page 37)

```
Using the treasury stock method, we first calculate that the company would have received $1,050,000 ($35 for each of the 30,000 options exercised) if all the options had been exercised. The options would no longer be outstanding; instead, 30,000 shares of common stock would be outstanding. Under the treasury stock method, we assume that shares would be repurchased with the cash received upon exercise of the options. At an average market price of $55 per share, the $1,050,000 proceeds from option exercise, the company could have repurchased 19,091 shares. Therefore, the incremental number of shares issued is 10,909 (calculated as 30,000 minus 19,091).
```
Reference: EXAMPLE 11: A Diluted EPS Calculation Using the Treasury Stock Method for Options, Solution (Page 37)

```
                          Basic EPS    Diluted EPS Using
                                     Treasury Stock Method
Net income                $2,300,000   $2,300,000
Numerator                 $2,300,000   $2,300,000
Weighted average number of shares
outstanding               800,000      800,000
If converted              0            10,909
Denominator               800,000      810,909
EPS                       $2.88        $2.84
```
Reference: Exhibit 13: Calculation of Diluted EPS for Hihotech Company Using the Treasury Stock Method: Case of Stock Options (Page 38)

```
If the options had been exercised, the company would have received $1,050,000. If this amount had been received from the issuance of new shares at the average market price of $55 per share, the company would have issued 19,091 shares. IFRS refer to the 19,091 shares the company would have issued at market prices as the inferred shares. The number of shares issued under options (30,000) minus the number of inferred shares (19,091) equals 10,909. This amount is added to the weighted average number of shares outstanding of 800,000 to get diluted shares of 810,909. Note that this is the same result as that obtained under US GAAP; it is just derived in a different manner.
```
Reference: EXAMPLE 12: Diluted EPS for Options under IFRS, Solution (Page 38)

```
If the 20,000 shares of convertible preferred had each converted into 3 shares of the company's common stock, the company would have had an additional 60,000 shares of common stock (3 shares of common for each of the 20,000 shares of preferred). If the conversion had taken place, the company would not have paid preferred dividends of $200,000 ($10 per share for each of the 20,000 shares of preferred). The effect of using the if-converted method would be EPS of $3.13, as shown in Exhibit 14. Because this is greater than the company's basic EPS of $3.10, the securities are said to be antidilutive and the effect of their conversion would not be included in diluted EPS. Diluted EPS would be the same as basic EPS (i.e., $3.10).
```
Reference: EXAMPLE 13: An Antidilutive Security, Solution (Page 39)

```
                          Basic EPS    Diluted EPS Using
                                     If-Converted Method
Net income                $1,750,000   $1,750,000
Preferred dividend        -200,000     0
Numerator                 $1,550,000   $1,750,000
Weighted average number of shares
outstanding               500,000      500,000
If converted              0            60,000
Denominator               500,000      560,000
EPS                       $3.10        $3.13
                          -Exceeds basic EPS; security is antidilutive and, therefore, not included. Reported diluted EPS= $3.10.
```
Reference: Exhibit 14: Calculation for an Antidilutive Security (Page 39-40)

```
Panel A: Income Statements for Companies A, B, and C ($)
                           A             B             C
Sales                      $10,000,000   $10,000,000   $2,000,000
Cost of sales              3,000,000     7,500,000     600,000
Gross profit               7,000,000     2,500,000     1,400,000
Selling, general, and administrative expenses 1,000,000     1,000,000     200,000
Research and development   2,000,000     —             400,000
Advertising                2,000,000     —             400,000
Operating profit           2,000,000     1,500,000     400,000
```
Reference: Exhibit 15: Panel A: Income Statements for Companies A, B, and C ($) (Page 41-42)

```
Panel B: Common-Size Income Statements for Companies A, B, and C (%)
                           A      B      C
Sales                      100%   100%   100%
Cost of sales              30     75     30
Gross profit               70     25     70
Selling, general, and administrative expenses 10     10     10
Research and development   20     0      20
Advertising                20     0      20
Operating profit           20     15     20
```
Reference: Exhibit 15: Panel B: Common-Size Income Statements for Companies A, B, and C (%) (Page 42)

```
                          Energy  Materials Industrials Consumer       Consumer   Health Care
                                                    Discretionary  Staples
Number of observations    34      27        69        81             34         59
Gross Margin              37.7%   33.0%     36.8%     37.6%          43.4%      59.0%
Operating Margin          6.4%    14.9%     13.5%     11.0%          17.2%      17.4%
Net Profit Margin         4.9%    9.9%      8.8%      6.0%           10.9%      7.2%
```
Reference: Exhibit 16: Median Common-Size Income Statement Statistics for the S&P 500 Classified by S&P/MSCI GICS Sector Data for 2017 (Page 42)

```
                          Financials Information   Telecommunication Utilities Real Estate
                                     Technology   Services
Number of observations    63         64           4                29        29
Gross Margin              40.5%      62.4%        56.4%            34.3%     39.8%
Operating Margin          36.5%      21.1%        15.4%            21.7%     30.1%
Net Profit Margin         18.5%      11.3%        13.1%            10.1%     21.3%
```
Reference: Income Statement Ratios (Page 43)

```
Net profit margin = Net income
                    -----------
                    Revenue
```
Reference: Net profit margin formula (Page 43)

```
Gross profit margin = Gross profit
                      -----------
                      Revenue
```
Reference: Gross profit margin formula (Page 43)

```
                       2017         2016         2015
                       $        %    $        %    $        %
Revenue                56,444   100.0  45,517   100.0  43,604   100.0
Cost of sales          (21,386) (37.9) (17,803) (39.1) (17,137) (39.3)
Gross profit           35,058   62.1   27,715   60.9   26,467   60.7
Distribution expenses  (5,876)  (10.4) (4,543)  (10.0) (4,259)  (9.8)
Sales and marketing expenses (8,382)  (14.9) (7,745)  (17.0) (6,913)  (15.9)
Administrative expenses(3,841)  (6.8)  (2,883)  (6.3)  (2,560)  (5.9)

Profit from operations 17,152   30.4   12,882   28.3   13,904   31.9
Finance cost           (6,885)  (12.2) (9,382)  (20.6) (3,142)  (7.2)
Finance income         378      0.7    818      1.8    1,689    3.9
Net finance income/(cost) (6,507)  (11.5) (8,564)  (18.8) (1,453)  (3.3)
Share of result of associates and joint ventures 430 0.8 16 0.0 10 0.0
Profit before tax      11,076   19.6   4,334    9.5    12,461   28.6
Income tax expense     (1,920)  (3.4)  (1,613)  (3.5)  (2,594)  (5.9)
Profit from continuing operations 9,155 16.2 2,721 6.0 9,867 22.6
Profit from discontinued operations 28 0.0 48 0.1 -- --
Profit of the year     9,183    16.3   2,769    6.1    9,867    22.6
```
Reference: Exhibit 17: AB InBev's Margins: Abbreviated Common-Size Income Statement (Page 44)

```
If the company's actual ending shareholders' equity is €227 million, then €10 million [€227− (€200 + €20 – €3)] has bypassed the net income calculation by being classified as other comprehensive income.
```
Reference: EXAMPLE 14: Other Comprehensive Income, Solution to 1 (Page 47)

```
Company A    Company B
Price              $35          $30
EPS                $1.60        $0.90
P/E ratio          21.9x        33.3x
OCI (loss) $ million ($16.272)    $(1.757)
Shares (millions)  22.6         25.1
OCI (loss) per share $(0.72)      $(0.07)
Comprehensive EPS = EPS + OCI per share $ 0.88 $0.83
Price/Comprehensive EPS ratio 39.8x 36.1x
```
Reference: EXAMPLE 15: Other Comprehensive Income in Analysis, Solution (Page 48)

```
Net revenue is revenue for goods sold during the period less any returns and allowances, or $1,000,000 minus $100,000 = $900,000.
```
Reference: Solutions, Question 5 (Page 56)

```
Under the weighted average cost method:
October purchases   10,000 units   $100,000
November purchases  5,000 units    $55,000
Total              15,000 units   $155,000

$155,000/15,000 units = $10.3333
$10.3333 × 12,000 units = $124,000
```
Reference: Solutions, Question 9 (Page 56)

```
Straight-line depreciation would be ($600,000 – $50,000)/10, or $55,000.
```
Reference: Solutions, Question 11 (Page 56)

```
Double-declining balance depreciation would be $600,000 × 20 percent (twice the straight-line rate).
```
Reference: Solutions, Question 12 (Page 56)

```
The weighted average number of shares outstanding for 2009 is 1,050,000. Basic earnings per share would be $1,000,000 divided by 1,050,000, or $0.95.
```
Reference: Solutions, Question 16 (Page 57)

```
Diluted EPS = (Net income)/(Weighted average number of shares outstanding + New common shares that would have been issued at conversion)
= $200,000,000/[50,000,000 + (2,000,000 × 2)]
= $3.70
```
Reference: Solutions, Question 18 (Page 57)

```
Proceeds from option exercise = 100,000 × $20 = $2,000,000
Shares repurchased = $2,000,000/$25 = 80,000
The net increase in shares outstanding is thus 100,000 – 80,000 = 20,000. Therefore, the diluted EPS for CWC = ($12,000,000 – $800,000)/2,020,000 = $5.54.
```
Reference: Solutions, Question 19 (Page 57)

```
LB's basic EPS is $1.22 [= ($3,350,000 – $430,000)/2,400,000].
```
Reference: Solutions, Question 20 (Page 57)

```
Shares outstanding    1,000,000
Options exercises     10,000
Treasury shares purchased (6,667)
Denominator          1,003,333
```
Reference: Solutions, Question 21 (Page 58)

```
Other comprehensive income = Unrealized gain on available-for-sale securities – Unrealized loss on derivatives accounted for as hedges + Foreign currency translation gain on consolidation
= $5 million – $3 million + $2 million
= $4 million

Alternatively,
Comprehensive income – Net income = Other comprehensive income
Comprehensive income = (Ending shareholders equity – Beginning shareholders equity) + Dividends
= ($493 million – $475 million) + $1 million
= $18 million + $1 million = $19 million
Net income is $15 million so other comprehensive income is $4 million.
```
Reference: Solutions, Question 24 (Page 58)