# Heart Failure Prediction ❤⚡
 
# 📁Dataset:

<p align="center">
    <img src="https://github.com/mill-ornrakorn/Heart-Failure-Prediction/blob/main/pic%20for%20readme/dataset.png?raw=true" alt= "dataset" >
</p>

ข้อมูลนี้เกี่ยวกับภาวะหัวใจล้มเหลว มาจาก [Heart Failure Prediction ใน kaggle](https://www.kaggle.com/datasets/bhavikjikadara/heart-failure-prediction) ซึ่งประกอบไปด้วย label คือ 0 = ไม่เป็นภาวะหัวใจล้มเหลว และ 1 = มีภาวะหัวใจล้มเหลวแล้วเสียชีวิต

# 📊EDA (แปะมาบางส่วน):

- Label (จาก DEATH_EVENT column)
<p align="center">
    <img src="https://github.com/mill-ornrakorn/Heart-Failure-Prediction/blob/main/pic%20for%20readme/DEATH_EVENT_plot.png?raw=true" alt= "DEATH_EVENT_plot" >
</p>

จะเห็นว่าข้อมูลชุดนี้เป็น Imbalanced โดยที่ class 0 มีประมาณ 200 rows และ class 1 มีเกือบ 100 rows

- Correlation
<p align="center">
    <img src="https://github.com/mill-ornrakorn/Heart-Failure-Prediction/blob/main/pic%20for%20readme/corr.png?raw=true" alt= "corr" >
</p>

</br>

<details>
    <summary>Dashboard (Click here)</summary>
    <p align="center">
        <img src="https://github.com/mill-ornrakorn/Heart-Failure-Prediction/blob/main/pic%20for%20readme/dashboard.png?raw=true" alt= "dashboard" >
    </p>

<details>
    <summary>Dashboard filter by Class0 (Click here)</summary>
    <p align="center">
        <img src="https://github.com/mill-ornrakorn/Heart-Failure-Prediction/blob/main/pic%20for%20readme/dashboard_filterbyClass0.png?raw=true" alt= "dashboard_filterbyClass0" >
    </p>


</details>

<details>
    <summary>Dashboard filter by Class1 (Click here)</summary>
    <p align="center">
        <img src="https://github.com/mill-ornrakorn/Heart-Failure-Prediction/blob/main/pic%20for%20readme/dashboard_filterbyClass1.png?raw=true" alt= "dashboard_filterbyClass1" >
    </p>


</details>

หมายเหตุ: ใน powerbi ไม่มี Histogram มาให้ แต่มีส่วนเสริมให้ใช้แทน อาจทำให้กราฟดูยากบ้าง การดู Dashboard เลยแนะนำให้เปิดไฟล์ของ powerbi ดู จะดูได้ง่ายกว่าแบบรูปนะคะ

</details>

</br>



# 📝ตารางสรุปผล:

| No. |      Model         |         Dataset            |    Train set | Test set    | Description | Accuracy | Precision | Recall |  F1-Score | AUC |
|-----|:------------------:|---------------------------:|---------:|-----:|-----:|-----:|-----:|------:|------:|------:|
| 1   |    Decision Tree    |  ใช้ข้อมูลทั้งหมดเลย (Imbalanced)  | 70% = Class 0: 139 rows, Class 1: 70 rows |  30% = Class 0: 64 rows, Class 1: 26 rows | - | 80% | Class 0: 88%, Class 1: 63% | Class 0: 83%, Class 1: 73%  | Class 0: 85%, Class 1: 68%  | 78%
| 2   |   Random Forest    |  ใช้ข้อมูลทั้งหมดเลย (Imbalanced)  | 70% = Class 0: 139 rows, Class 1: 70 rows |  30% = Class 0: 64 rows, Class 1: 26 rows | ใช้จำนวน estimators = 78 | 90% | Class 0: 94%, Class 1: 81% | Class 0: 92%, Class 1: 85%  | Class 0: 93%, Class 1: 83%  | 94%
| 3   |   XGBoost    |  ใช้ข้อมูลทั้งหมดเลย (Imbalanced)  | 70% = Class 0: 139 rows, Class 1: 70 rows |  30% = Class 0: 64 rows, Class 1: 26 rows | - | 88% | Class 0: 93%, Class 1: 76% | Class 0: 89%, Class 1: 85%  | Class 0: 91%, Class 1: 80%  | 93%


- Feature Importance from Random Forest
<p align="center">
    <img src="https://github.com/mill-ornrakorn/Heart-Failure-Prediction/blob/main/pic%20for%20readme/FeatureImportance.png?raw=true" alt= "Feature Importance" >
</p>
