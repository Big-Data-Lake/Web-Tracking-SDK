# Web-Tracking-SDK

## Usage
### Import file

    <script type="text/javascript" src="https://web-sdk.ikala-c4m.io/ika.js"></script>

### Track every page

Add scipt in every page you want to track with `IKA_ID` from iKala like below:

    ika.init('{IKA_ID}')

### Set User

Set User ID after user login like below:

    ika.setUserId('{USER_ID}')
    
### Track Event

    ika.addEvent('login', { 'loginType': loginType });
    ika.addEvent('addcart',{'itemId':id,'quantity':qty,'price':price});

### Event doc

<table>
<thead><tr><th>Name</th><th>Key</th><th>Remark</th></tr></thead><tbody>
<tr><td>click</td><td>which</td><td>自定義名稱</td></tr>
<tr><td rowspan=2>searchWord</td><td>word</td><td>搜尋關鍵字</td></tr>
<tr><td>resultSize</td><td>搜尋結果筆數/數量</td></tr>
<tr><td rowspan=5>searchFilter</td><td>itemCateId</td><td>搜尋勾選的商品分類 ID</td></tr>
<tr><td>payType</td><td>搜尋勾選的搜尋付款方式</td></tr>
<tr><td>shipType</td><td>搜尋勾選的運送方式</td></tr>
<tr><td>minPrice</td><td>搜尋勾選的價格區間 Min</td></tr>
<tr><td>maxPrice</td><td>搜尋勾選的價格區間 Max</td></tr>
<tr><td rowspan=5>addWish</td><td>itemCateId</td><td>商品分類 ID</td></tr>
<tr><td>itemId</td><td>商品 ID</td></tr>
<tr><td>sku</td><td>SKU</td></tr>
<tr><td>currency</td><td>貨幣</td></tr>
<tr><td>price</td><td>金額</td></tr>
<tr><td rowspan=5>removeWish</td><td>itemCateId</td><td>商品分類 ID</td></tr>
<tr><td>itemId</td><td>商品 ID</td></tr>
<tr><td>sku</td><td>SKU</td></tr>
<tr><td>currency</td><td>貨幣</td></tr>
<tr><td>price</td><td>金額</td></tr>
<tr><td rowspan=6>addCart</td><td>itemCateId</td><td>商品分類 ID</td></tr>
<tr><td>itemId</td><td>商品 ID</td></tr>
<tr><td>sku</td><td>SKU</td></tr>
<tr><td>quantity</td><td>數量</td></tr>
<tr><td>currency</td><td>幣別</td></tr>
<tr><td>price</td><td>金額</td></tr>
<tr><td rowspan=6>removeCart</td><td>itemCateId</td><td>商品分類 ID</td></tr>
<tr><td>itemId</td><td>商品 ID</td></tr>
<tr><td>sku</td><td>SKU</td></tr>
<tr><td>quantity</td><td>數量</td></tr>
<tr><td>currency</td><td>幣別</td></tr>
<tr><td>price</td><td>金額</td></tr>
<tr><td>viewItemList</td><td>itemIdList</td><td>商品分類 ID清單</td></tr>
<tr><td rowspan=3>viewItem</td><td>itemCateId</td><td>商品分類 ID</td></tr>
<tr><td>itemId</td><td>商品 ID</td></tr>
<tr><td>sku</td><td>SKU</td></tr>
<tr><td rowspan=3>getCoupon</td><td>couponId</td><td>折價券 ID </td></tr>
<tr><td>couponType</td><td>折價券類型</td></tr>
<tr><td>couponAmount</td><td>折價券面額</td></tr>
<tr><td rowspan=3>useCoupon</td><td>couponId</td><td>折價券 ID </td></tr>
<tr><td>couponType</td><td>折價券類型</td></tr>
<tr><td>couponAmount</td><td>折價券面額</td></tr>
<tr><td rowspan=5>confrimCartList</td><td>itemIdList</td><td>商品 ID 列表</td></tr>
<tr><td>skuList</td><td>SKU 列表</td></tr>
<tr><td>quantity</td><td>數量</td></tr>
<tr><td>currency</td><td>幣別</td></tr>
<tr><td>price</td><td>金額</td></tr>
<tr><td rowspan=2>checkoutProcess</td><td>step</td><td>階段</td></tr>
<tr><td>option</td><td>選項</td></tr>
<tr><td>login</td><td>loginType</td><td>登入類型</td></tr>
<tr><td>register</td><td>registerType</td><td>註冊類型</td></tr>
</tbody></table>

### Track Transaction

    ika.addTransaction('purchase', { 'orderId': id, 'payType': payType, 'revenue': price });
    
### Transaction doc
<table>
<thead>
<tr>
<th>Name</th>
<th>Key</th>
<th>Remark</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan=6>purchase</td>
<td>orderId</td>
<td>訂單成立編號</td>
</tr>
<tr>
<td>payType</td>
<td>付款方式</td>
</tr>
<tr>
<td>shipType</td>
<td>運送方式</td>
</tr>
<tr>
<td>shipCost</td>
<td>運費</td>
</tr>
<tr>
<td>revenue</td>
<td>總金額 (含運費)</td>
</tr>
<tr>
<td>currency</td>
<td>幣別</td>
</tr>
<tr>
<td rowspan=3>refund</td>
<td>orderId</td>
<td>原訂單編號</td>
</tr>
<tr>
<td>refundId</td>
<td>退貨訂單編號</td>
</tr>
<tr>
<td>reason</td>
<td>退貨原因描述</td>
</tr>
</tbody>
</table>

    
