# pagination-
pagination 


注意事項

正式安裝之前仍有兩件事項需要注意：

這個工具必須讀取部落格的 feed，因此公開的部落格才能正常執行，請檢查後台 → 設定 → 其他 → 允許網誌資訊提供 → 是否為「完整」
後台設定每頁顯示的文章數，必須與小工具的設定一致，請檢查後台 → 設定 → 文章和留言 → 最多顯示 → 這裡的數字請與小工具的參數吻合。


接著請搜尋 </body> 這個字串，找到後在此字串的前一行，插入以下程式碼

<!-- 數字分頁 + Ajax 動態載入 start-->
<script>//<![CDATA[
var pageNav = {
perPage: 5, // 每頁顯示的文章數
numPages: 5, // 要顯示數字的按鈕數量
ajax: "Y", // 頁面是否動態載入, 不要則改成 "N"
firstText: "First",
lastText: "Last",
prevText: "« Previous",
nextText: "Next »"
};
$.getScript("https://drive.google.com/file/d/1u-QQxHCNTLxxyGGKtKjjhg2IH8psfFwJ/view");
//]]></script>

以下參數修改請參照以上程式碼行號：

D：紅色參數代表每頁顯示的文章數，請跟「二、準備動作」→「3. 注意事項」後台設定的數字一致。

E：紅色參數代表換頁數字按鈕要顯示的數量，若實際的頁數超過設定的數字時，會自動隱藏。

2015.1.13 新增： F 行紅色參數 "Y" 代表頁面使用動態載入，若不使用動態載入請改成 "N"。

G~J：字串可改為中文，例如 "第一頁"、"最後一頁"、"前一頁"、"下一頁"。





