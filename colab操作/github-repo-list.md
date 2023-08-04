# Google Colab 使用

主要連結：[link](https://colab.research.google.com/drive/1wBm0-XT8mC7LooZroloJPNU4fTKGwriu?usp=sharing)

步驟：
- 點擊後，登入Google帳戶，應該就可以看到頁面
![image](https://i.imgur.com/Us2DKKk.png)
- 複製該colab筆記本到自己的google drive空間，就可以隨意玩該colab而不用擔心操作到我原本的colab：
![image](https://i.imgur.com/cEm4YWx.png)
- 主要運行方式就是按code框左上角的「運行」按鈕。這個repo要先運行一下第一個函數，讓整個空間註冊該函數
![image](https://i.imgur.com/in0CC8Y.png)
- 然後就可以拉到最下面，新增code
![image](https://i.imgur.com/weEfOPS.png)
- 跟上面的code一樣，複製函數 `getGithubRepoByQuery`
    - 第一個參數代表想查詢的關鍵詞，ex：`"LLM"`
    - 第二個為要爬取的總頁數，由於一頁為100筆資料，加上github api的次數限制，大概30～40頁就好（而且已經以stars數做排序，所以越後面的repo星數越少）
- 運行完後，可以到旁邊的存儲空間下載輸出好的`.xlsm`檔
![image](https://i.imgur.com/kGfIAkM.png)