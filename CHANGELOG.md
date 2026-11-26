# Changelog

## 0.1.24
⚠️ IMPORTANT for all users (Windows, macOS and Linux/Ubuntu) with an installer version older than 0.1.21: please download and install the app again from https://www.databloom.it/cactus.html - you can check your installer version in the Help & Support page.

🌵 New
- Regression test tab redesigned: Model Trained and Test Set boxes, and all results (metrics, predictions with residuals, plots) in a single box 🌵
- Measured vs Predicted and Residuals vs Fitted plots with settings (colours by factor, symbols, sample names, line colours) in calibration, CV and test; train samples filled, test samples open
- KNN: the number of PCs is tuned in CV, new Nearest Neighbors Distance Plot, probabilities and ROC curves in the test
- Classification test tab: Test Set box with known and unknown classes, and a Summary tab in Model Calibration
- Regression: a Summary tab in Model Calibration (MLR, PCR, PLS) with the same information as the Model Trained box of the test
- SIMCA test tab redesigned like Classification: Model Trained and Test Set boxes, and a Prediction tab with the Accepted/Rejected decision of every sample
- One Class Modeling (SIMCA) is available right after Approve Dataset: it has its own preprocessing, so the global Preprocessing step is no longer needed
- SIMCA cross-validation is much faster, with the same results 🌵
- Help & Support: download your settings to a file, or load a settings file received from someone else (e.g. a teacher preparing the app for a class) 🌵
- Unsupervised: a Model Trained box for PCA, HCA, K-means and t-SNE, with the number of components and the explained variance when PCA is performed first; PCA Download button next to Calculate🌵
- Classification test tab: new Metrics per Class tab
- Cross-validation: the fold boxplot has its own larger tab (Classification, Regression and SIMCA), and its points are easier to hover
- MLR: info button on the Model Summary box, with a simple explanation of Coefficients, Model Statistics, VIF and Assumptions
- HCA and K-means: Download button next to Calculate, like PCA, with the cluster of every sample in Excel 🌵
- New app icon on Windows and Linux, easier to see on dark backgrounds (reinstall needed)

🌵 Fixed
- LDA and QDA: Fit Best Model now uses the chosen number of PCs
- Test results are cleared when the model is retrained or the data are reset
- Calibration metrics are now labelled with _C (RMSE_C, R²_C, ...), like _CV for cross-validation
- ROC curves removed from cross-validation
- Statistics: the non-parametric alternative to the t-test is now labelled Mann-Whitney U (Wilcoxon rank-sum), with the Mann & Whitney (1947) reference
- Split: DUPLEX now keeps replicates together when a grouping factor is chosen (it was ignored), with the train/test proportion counted on groups
- Baseline (ALS): the default lambda is now 1e6; the old default (6) barely smoothed the baseline and removed part of the peaks
- Categorical colours are saved as HEX codes: some colours picked in Settings were saved by name (e.g. darkorange1) and not shown correctly
- Linux: the app window now shows the Cactus icon and name in the dock (reinstall needed)
- SIMCA: components in the Scree Plot are in the right order (PC1, PC2, ... PC10)
- Classification with two classes: Sensitivity, Specificity, Precision and F1 are now the average of the two classes, as with three or more classes, instead of the values of the first class only: results differ from previous versions. The values of each class are in Metrics per Class
- Confusion matrices and the Split class plot: classes named with numbers (e.g. 0 and 1) no longer get a numeric axis with values like 0.5
- Missing values: imputing a column of whole numbers no longer crashes the app
- New error window when the app stops: it now explains what happened and how to send us the log file
- PLS regression test: if the test set cannot be preprocessed like the training set (e.g. missing variables), a message explains it instead of showing wrong scores
- MLR: the Influence box now shows Leverage vs Studentized residuals and Cook's distance with their limits (it showed the residuals again)
- MLR: Model Statistics shows the Residual standard error (σ) under its own name, instead of a second RMSE_C with a different value
- MLR: p-values in the Assumptions table are shown in short scientific notation (e.g. 4.103e-03) instead of a long row of digits

Thanks for using Cactus! 🌵🌵🌵

## 0.1.23
⚠️ IMPORTANT for all users (Windows, macOS and Linux/Ubuntu) with an installer version older than 0.1.21: please download and install the app again from https://www.databloom.it/cactus.html - you can check your installer version in the Help & Support page.

🌵 New
- ROC curves in cross-validation for all classification models 🌵
- PLS-DA: ROC curves in the Test tab too, also with the Max, Centroids and Mahalanobis rules (computed on the predicted Y values)
- LDA: the test summary shows how many principal components were used when PCA is applied before LDA
- Model titles are now written in full (e.g. Linear Discriminant Analysis)

🌵 Fixed
- ROC curves now work with two classes and when the test set does not contain every class, and each class shows its own AUC
- Venetian blinds and Contiguous blocks cross-validation no longer crash the app when some folds miss a class: a message suggests a different CV method
- LDA axes are now named as canonical variates (CV1, CV2, ...)
- Class probability plot: train and test symbols were swapped in QDA and PLS-DA
- The "Show misclassified samples" title in the plot settings is now readable in the light theme
- The split visualization box can now be maximized

Thanks for using Cactus! 🌵🌵🌵

## 0.1.22
⚠️ IMPORTANT for all users (Windows, macOS and Linux/Ubuntu) with an installer version older than 0.1.21: please download and install the app again from https://www.databloom.it/cactus.html - you can check your installer version in the new Help & Support page.

🌵 New
- Test set results: the new Prediction tab lists every test sample with its predicted class, correct ones in green and wrong ones in red, with Excel export 🌵
- QDA test results now have the same tabs as the other models: metrics, confusion matrix, predictions and ROC curves
- PLS-DA: regression coefficients are now shown in the Test tab too, and the coefficient plot shows the selected class in its title
- PLS-DA: option to show or hide the values on the VIP bars in the Test tab
- Excel export for the test set metrics

🌵 Fixed
- PLS-DA, QDA and KNN no longer fail when the test set contains classes that are not in the training set
- Excel export now includes all rows of the table, not only the visible page

Thanks for using Cactus! 🌵🌵🌵

## 0.1.21

⚠️ IMPORTANT for all users (Windows, macOS and Linux/Ubuntu) with an installer version older than 0.1.21: please download and install the app again from https://www.databloom.it/cactus.html - you can check your installer version in the new Help & Support page.

🌵 New
- New Help & Support page: user guide, bug reports, feedback form, app and installer versions, and a button to download the log file to attach to your reports
- Loading animations now show a growing cactus 🌵

🌵 Fixed
- Classification no longer crashes when the response column contains only one class: a message explains what to do

Thanks for using Cactus! 🌵🌵🌵

## 0.1.20

⚠️ IMPORTANT for all users (Windows, macOS and Linux/Ubuntu): please download and install this version from https://www.databloom.it/cactus.html - the in-app update does not include the new update window.

🌵 Fixed
- The update window is now larger and resizable, so release notes are easy to read 🌵

Thanks for using Cactus! 🌵🌵🌵

## 0.1.19

⚠️ IMPORTANT for all users (Windows, macOS and Linux/Ubuntu) with a version older than 0.1.19: please download and install the app again from https://www.databloom.it/cactus.html - the in-app update does not include the faster startup and the new installer fixes.

🌵 New
- Linux: the installer now works on Ubuntu 22.04, 24.04 and 26.04 🌵
- Faster startup: the login window appears as soon as the app is ready
- XY Line Plot in the bivariate visualization
- Correlation heatmap with a colour scale that adapts to the data
- PCA loadings shown as a scatter plot
- Excel export of cross-validation tables and of cross-validation warnings
- Back button to return to the Split / No split choice
- Categorical colours are never repeated, with any number of colours 🌵

🌵 Fixed
- macOS: missing R packages (scatter matrix, heatmaps, glmnet models)
- Cross-validation: wrong samples flagged as misclassified, faster computation, readable message when every fold fails
- SIMCA Cross-validation by replicates now sees the grouping columns
- Legends, marker symbols and class order in scatter plots
- Boxplots and violin plots grouped by sub-levels; multivariate boxplots with Tukey whiskers
- Pipeline step parameters no longer reset when the pipeline changes
- Dark theme readability and drop-down menus hidden behind sliders
- Maximized boxes no longer grow endlessly

Thanks for using Cactus! 🌵🌵🌵
