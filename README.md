# Anaconda-VScode
這是用來記錄如何將Anaconda的jupyer套在VScode環境中

jupyer裡面會有tensorflow、numpy、其餘等等......的函式庫

我所使用的方式是利用Anaconda建立一個虛擬環境，讓VScode去選取"虛擬環境"當作解譯器執行


希望這篇能幫助需樣在VScode中使用深度學習(DL，Deep learning)的人

內容僅供參考

參考網站：
* [Anaconda｜建立虛擬環境(Environments)](https://songzhu1030.medium.com/anaconda-%E5%BB%BA%E7%AB%8B%E8%99%9B%E6%93%AC%E7%92%B0%E5%A2%83-environments-2d1d78d9ccf0)
* [快速安裝Tensorflow-GPU 2.1.0 搭配VS Code](https://hackmd.io/@eric60305/SyKKaIzFw)

## CPU使用版本
系統 - windows 10 X64
* python = 3.6.10
* Anaconda = 2.5.2
* tensorflow = 2.0.0
* numpy = 1.19.5 、1.17.0
* keras = 2.3.1
  
## GPU使用版本
系統 - windows 10 X64
顯卡 - GTX 1050 ti
* python = 3.6.10
* Anaconda = 2.5.2
* tensorflow = 2.0.0
* numpy = 1.19.5 、1.17.0
* keras = 2.3.1
* 
>[!Tip]
>未來有機會再更新
****

## 事前準備(下載檔案)
1. python - [download](https://www.python.org/downloads/)
2. Anaconda3 - [download](https://www.anaconda.com/download)
3. VS Code - [download](https://code.visualstudio.com)
> [!NOTE] 
> 我python是安裝3.7.0-amd64，Anaconda3只能下載到最新的版本，VScode也一樣。
> 建議一律按照原先安裝程式時預設的位置，避免發生不必要的麻煩。

## 步驟
1. 在Anaconda建立虛擬環境，可以去看參考網站

   建立虛擬機
   ```
   conda create --name XXXXXXXX python=3.6 anaconda
   ```
   
   XXXXXXXX = 你的虛擬機名稱

   建立時會詢問是否要安裝其他函示庫，一律都輸入Y同意

   在虛擬機安裝tensorflow=2.0.0
   ```
   conda install tensorflow=2.0.0
   ```
   安裝numpy=1.19.5
   ```
   conda install numpy=1.19.5
   ```
   安裝keras
   ```
   conda install keras
   ```
   
2. 將VScode 安裝延伸模組

   - Jupyter 
   -  Python 
   -  Pylance

3. 找到虛擬機的資料夾

   會在Anaconda3/envs裡面

   找到你所建立的虛擬機資料夾

   裡面會有python.exe的應用程式

   把這個資料夾的路徑記住，待會VScode要使用到
   
4. 到VScode將虛擬機套入進去

   開啟VScode，然後按下F1，接著輸入
   ```
   python select interpreter
   ```
   把剛剛虛擬機的python.exe路徑複製上去

   anacnoda3\envs\XXXXXXXX\python.exe
   

6. 寫一段小程式，測試tensorflow是否安裝成功
   ```
   import tensorflow as tf
   print(tf.__version__)
   
   import numpy as np
   print(np.__version__)
   ```

