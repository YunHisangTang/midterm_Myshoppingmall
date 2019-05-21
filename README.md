# midterm_Myshoppingmall
作者: 湯昀翔 r07631005
1. 題目名稱 :  midterm_Myshoppingmall

[https://github.com/YunHisangTang/midterm_Myshoppingmall](https://github.com/YunHisangTang/midterm_Myshoppingmall)

2. 一句話描述這個 project 在做什麼 : 簡化版的購物網站

3. 使用/操作方式 :

> 到下載的資料夾下:
> npm install 
> npm start

4. 其他說明 :
	* 使用 : NodeJS / Express / MongoDB
	* 功能 : 
		* 透過點擊將商品放入購物車中
		* 在購物車頁面計算總金額
		* 結算頁面能進行訂單的下訂
		* 有註冊會員功能
5. 使用與參考之框架/模組/原始碼 :
	
	* https://developerhandbook.com/mongodb/connect-mongo-atlas-mongoose/?fbclid=IwAR3yAQn3EU11XjDVtSYb9kE5uCavCinX4mUbLUbFHhAmoIuMEmvAAJ9OORo
	* mschwarzmueller : [https://github.com/mschwarzmueller/nodejs-shopping-cart-tutorial](https://github.com/mschwarzmueller/nodejs-shopping-cart-tutorial)

6. 我的貢獻 :
	基本上是看著網路上的教學從零慢慢打起，主要是後端的部分，前端比較少設計。
7. 心得 :
	原本想要再加入老師上課教的聊天室，但卡在Stripe金流的部分，就沒繼續寫上。
	
8. 架構:

* 20190521_v1 :
   * bin
   * config : 
      * passport.js (User的登入和註冊，E-mail需正確格式、密碼需4位)
   * models : 
      * cart.js (進行購物車內的金額計算)
      * product.js (上傳到mongoDB.Atlas的商品模板)
      * user.js (上傳到mongoDB.Atlas的User的模板)
   * public
	  * javascripts/checkout.js (連動Stripe帳戶進行商品的付款(尚未成功))，目前開放輸入任何資料都能結帳完成。)
	  * stylesheets/style.css	
   * routes
     * index.js(router做甚麼動作都寫在這)
     * user.js(router做User的登入和註冊動作都寫在這)
   * seed
     *  product-seeder.js(上架商品目錄，用node product-seeder.js就能將商品放到mongoDB中)
   * views (前端)
     *  layout (整體網頁框架)
     *  partials (最上面的目錄Bar部分)
     *  shop(商品頁面、結帳、購物車部分)
     *  user(User的登入和註冊部分)
     *  error.hbs (錯誤顯示部分)
   * app.js(後端所需模組)
   * package-lock.json
   * package.json
