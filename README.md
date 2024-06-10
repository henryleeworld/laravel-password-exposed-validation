# Laravel 11 密碼暴露驗證

引入 dilneiss 的 laravel-password-exposed-validation-rule 套件來擴增密碼暴露驗證，近年來大型網路服務被駭客入侵，竊取用戶個資的新聞層出不窮，只要一不小心，可能就是數十萬，甚至數百萬筆使用者資料被公佈在網路上，雖然大部分的服務都會以加密方式來處理使用者的密碼，但要是密碼組合太過簡單，也是有可能遭到破解的。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令的 __migrate__ 來執行所有未完成的遷移。
```sh
$ php artisan migrate
```
- 執行安裝 Vite 和 Laravel 擴充套件引用的依賴項目。
```sh
$ npm install
```
- 執行正式環境版本化資源管道並編譯。
```sh
$ npm run build
```
- 在瀏覽器中輸入已定義的路由 URL 來訪問，例如：http://127.0.0.1:8000。
- 你可以經由 `/register` 來進行註冊。

----

## 畫面截圖
![](https://i.imgur.com/rlIG1IH.png)
> 建議在密碼已知被竊取的情況下才需更換密碼

![](https://i.imgur.com/WmTNbxl.png)
> 藉由增加密碼的長度和複雜性，可以大大增加破解密碼所需的時間和資源
