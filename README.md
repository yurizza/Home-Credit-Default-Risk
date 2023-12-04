# Home-Credit-Default-Risk

Business Problem : The lending company (Home Credit) is facing challenges in assessing credit risk for potential borrowers. To enhance credit decisions, the company wishes to implement a machine learning model that can predict customers' ability to repay loans based on historical data and other attributes.

Objective : Implementing a predictive model using the Linear Regression algorithm aims to enhance the company's ability to assess the credit risk of potential borrowers based on historical data and other attributes

Data Understanding :
application_{train|test}.csv
This is the main table, broken into two files for Train (with TARGET) and Test (without TARGET).
Static data for all applications. One row represents one loan in our data sample.
previous_application.csv
All previous applications for Home Credit loans of clients who have loans in our sample.
There is one row for each previous application related to loans in our data sample
bureau.csv
All client's previous credits provided by other financial institutions that were reported to Credit Bureau (for clients who have a loan in our sample).
For every loan in our sample, there are as many rows as number of credits the client had in Credit Bureau before the application date
*All data will be joined based on the 'SK_ID_CURR' column.
*For the 'bureau' and 'previous_application' datasets, aggregation will be performed.

Conclusion :
Analisis hasil evaluasi model logistik regresi menunjukkan bahwa meskipun akurasi keseluruhan mencapai 78%, model memiliki tantangan dalam memprediksi secara konsisten antara kelas positif (default risk pada Home Credit) dan negatif (tidak default risk). Presisi yang rendah (16%) dan recall yang lebih tinggi (42%) menunjukkan bahwa model cenderung kesulitan mengidentifikasi dengan tepat kasus yang sebenarnya positif, dengan nilai AUC yang menengah (0.62). Ini memperlihatkan perlunya perhatian lebih lanjut untuk meningkatkan kinerja model, terutama dalam mengantisipasi risiko default pada Home Credit.
Logistic Regression
Evaluasi model XGBoost Classifier menunjukkan bahwa meskipun akurasinya tinggi (91%), model mengalami kesulitan dalam mengidentifikasi dengan tepat kasus positif (risiko default pada Home Credit) dengan nilai recall yang rendah (12%), sementara tingkat presisinya cukup (40%). Nilai F1-Score sebesar 18% mencerminkan keseimbangan antara presisi dan recall. Meski begitu, AUC dari Kurva ROC yang tinggi (0,76) menunjukkan kemampuan model dalam membedakan dengan baik antara kasus positif dan negatif. Dalam konteks risiko kredit Home Credit, perlu pertimbangan lebih lanjut untuk meningkatkan kemampuan model dalam mengenali kasus default dengan lebih akurat.
XGBoost Classifier
