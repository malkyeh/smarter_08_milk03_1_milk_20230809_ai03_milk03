# 牛隻乳量預測模型
使用牛隻的每小時活動力、生理、繁殖紀錄以及每小時環境的資料，去預測牛隻7天後的泌乳量。
模型：使用weka load model

左圖為輸入檔案(上面是欄位名稱以及它的type):
![](https://hackmd.io/_uploads/rkmmrHIG6.png)


右圖為輸出之結果範例，(下面是每一筆資料的數值):
![](https://hackmd.io/_uploads/SJZ4Er8z6.jpg)

輸入資料：須包含以下欄位每個小時的資料：MeasurementCount、NotActive、Ruminating、Eating、Active、HighActive、Temperature、Temp1、Temp2、Humi1、Humi2、Light、Thi1、Thi2。資料的欄位名稱命名方式為w1_小時_欄位 (舉例：w1_00_MeasurementCount)。最後包含牛隻出生日期(birth_days)、該次分娩胎次(parity)、前次DIM(LastTime_DIM)、7天后的泌乳量(milk_7)。型態都是numeric。檔案為arff 檔，可使用weka內建功能轉換。

此為整理完後的牛隻乳量預測檔
https://drive.google.com/file/d/1IC_NzWj_-9BGh-rUpHOdgN8xYrErGmh-/view?usp=drive_link
使用方式：
Open file -> 選擇你的資料 -> Classify -> 在Result list 按右鍵，選擇Load model > 選擇下載的模型 -> 在Test options 中選擇Supplied test set -> Set -> Open file -> 選擇你的資料 -> 確認Class 正確 -> 對model 點右鍵 -> Re-evaluate model on current test set