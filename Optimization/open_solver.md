# How to Install OpenSolver for Excel (Mac Version)

OpenSolver is a powerful open-source Excel plugin that enhances Excel’s Solver with advanced optimization capabilities. Follow the steps below to install OpenSolver on a Mac.

## 1. Download OpenSolver for Mac

- Visit the [OpenSolver website](https://opensolver.org/download/) and scroll down to the **OpenSolver for Mac** section.
- Download the latest version of **OpenSolver for Mac**. This file is typically a `.zip` archive.

## 2. Unzip the Downloaded File

- Locate the downloaded `.zip` file (usually in your **Downloads** folder).
- Right-click and choose **Open With > Archive Utility** to unzip the file. This will create a new folder containing `OpenSolver.xlam`.

## 3. Enable Macros in Excel

OpenSolver uses macros, so you'll need to ensure macros are enabled in Excel:

1. Open Excel.
2. In the top menu, click on **Excel** > **Preferences**.
3. Under **Security**, click on **Macro Security**.
4. Select **Enable all macros** to allow the macros OpenSolver requires.
5. Close the window to apply these settings.

## 4. Load OpenSolver in Excel

1. Open Excel and a new or existing workbook.
2. Click on the **Tools** menu in the Excel ribbon.
3. Select **Excel Add-ins** from the dropdown menu.
4. In the **Add-Ins** window, click the **Browse** button.
5. Navigate to the folder where you unzipped the OpenSolver files and select `OpenSolver.xlam`.
6. Click **OK**. You should now see an **OpenSolver** tab in your Excel ribbon.

## 5. Test OpenSolver

- Click on the **OpenSolver** tab in the Excel ribbon to confirm that the installation was successful.
- Try clicking **Model** or **Solve** to test its functionality.

## 6. Set OpenSolver to Open Automatically (Optional)

If you'd like OpenSolver to load automatically whenever you open Excel:
1. Go to **Finder** and open the folder where `OpenSolver.xlam` is located.
2. Press **Cmd** + **Shift** + **G**, and type `~/Library/Group Containers/UBF8T346G9.Office/User Content/Startup/Excel/`.
3. Drag the `OpenSolver.xlam` file into this folder. This will set it to load each time you open Excel.

## 7. Troubleshooting

If you encounter any issues:

- Ensure you're using a compatible version of Excel (OpenSolver is designed for Excel 2016 or newer on Mac).
- Visit the [OpenSolver troubleshooting page](https://opensolver.org/faq/) for help, or check their forums for solutions.

---

That's it! You've successfully installed OpenSolver for Excel on your Mac. You can now start solving linear and integer optimization problems with enhanced speed and capacity.