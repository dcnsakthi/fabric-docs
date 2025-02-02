---
title: Follow along in notebook
description: Steps to upload notebooks to use with get started tutorials.
author: sdgilley
ms.author: sgilley
ms.topic: include
ms.date: 10/11/2023
---

To explore and transform any pandas Dataframes in your notebook, launch Data Wrangler directly from the notebook.

>[!NOTE]
>Data Wrangler can not be opened while the notebook kernel is busy. The cell execution must complete prior to launching Data Wrangler.

1. Under the notebook ribbon **Data** tab, select **Launch Data Wrangler**. You'll see a list of activated pandas DataFrames available for editing. 
1. Select the DataFrame you wish to open in Data Wrangler. Since this notebook only contains one DataFrame, `pd`, select `pd`.

:::image type="content" source="../media/tutorial-data-science-explore-notebook/launch-data-wrangler.png" alt-text="Screenshot shows how to launch the data wrangler from a notebook.":::

Data Wrangler launches and generates a descriptive overview of your data. The table in the middle shows each data column. The **Summary** panel next to the table shows information about the DataFrame. When you select a column in the table, the summary updates with information about the selected column.  In some instances, the data displayed and summarized will be a truncated view of your DataFrame.  When this happens, you'll see warning image in the summary pane.  Hover over this warning to view text explaining the situation.

:::image type="content" source="../media/tutorial-data-science-explore-notebook/preview-inline.png" alt-text="Screenshot shows data wrangler overview." lightbox="../media/tutorial-data-science-explore-notebook/preview.png":::

Each operation you do can be applied in a matter of clicks, updating the data display in real time and generating code that you can save back to your notebook as a reusable function.  

The rest of this section walks you through the steps to perform data cleaning with Data Wrangler.

## Drop duplicate rows

On the left panel is a list of operations (such as **Find and replace**, **Format**, **Formulas**, **Numeric**) you can perform on the dataset. 

1. Expand **Find and replace** and select **Drop duplicate rows**.

    :::image type="content" source="../media/tutorial-data-science-explore-notebook/expand-section.png" alt-text="Screenshot shows drop duplicate rows under find and replace.":::

1. A panel appears for you to select the list of columns you want to compare to define a duplicate row. Select **RowNumber** and **CustomerId**.

    In the middle panel is a preview of the results of this operation. Under the preview is the code to perform the operation. In this instance, the data appears to be unchanged.  But since you're looking at a truncated view, it's a good idea to still apply the operation.

    :::image type="content" source="../media/tutorial-data-science-explore-notebook/drop-duplicate-inline.png" alt-text="Screenshot shows dropping duplicate rows in Data Wrangler." lightbox="../media/tutorial-data-science-explore-notebook/drop-duplicate.png":::


1. Select **Apply** (either at the side or at the bottom) to go to the next step.

### Drop rows with missing data

Use Data Wrangler to drop rows with missing data across all columns.

1. Select **Drop missing values** from **Find and replace**.
1. Choose **Select all** from the **Target columns**.

    :::image type="content" source="../media/tutorial-data-science-explore-notebook/drop-missing-inline.png" alt-text="Screenshot shows dropping missing rows in Data Wrangler." lightbox="../media/tutorial-data-science-explore-notebook/drop-missing.png":::

1. Select **Apply** to go on to the next step.

### Drop columns

Use Data Wrangler to drop columns that you don't need.

1. Expand **Schema** and select **Drop columns**.
1. Select **RowNumber**, **CustomerId**, **Surname**.  These columns appear in red in the preview, to show they're changed by the code (in this case, dropped.)

    :::image type="content" source="../media/tutorial-data-science-explore-notebook/drop-columns-inline.png" alt-text="Screenshot shows dropping columns in Data Wrangler." lightbox="../media/tutorial-data-science-explore-notebook/drop-columns.png":::

1. Select **Apply** to go on to the next step.

### Add code to notebook

Each time you select **Apply**, a new step is created in the **Cleaning steps** panel on the bottom left. At the bottom of the panel, select **Preview code for all steps** to view a combination of all the separate steps.

Select **Add code to notebook** at the top left to close Data Wrangler and add the code automatically. The **Add code to notebook** wraps the code in a function, then calls the function.  

:::image type="content" source="../media/tutorial-data-science-explore-notebook/add-to-notebook.png" alt-text="Screenshot shows preview code and where to access add to notebook.":::

> [!TIP]
> The code generated by Data Wrangler won't be applied until you manually run the new cell.