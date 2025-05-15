@babel/plugin-syntax-dynamic-import

@babel/plugin-transform-dynamic-import



@babel/preset-env：7.23.3



```json
{
    tenantId: "", // 云眸租户ID
    userId: "", // 云眸用户ID，对应开票的用户
	salerType: "", // 0:售卖方海康 1:售卖方非海康
    billNo:"", // 发票对应的订单号
    taxNo:"", // 销售方税号
    billDateTime:"", // 订单创建时间(yyyy-MM-dd HH:mm:ss)
    invoiceDetailsList: [ // 发票中的项目，即购买明细
        {
             goodsName:"", // 对应发票中的"项目名称"
    		goodsQuantity:"", // 对应发票中的"数量"
    		goodsTotalPriceTax:"", // 订单金额
            goodsSpecification:"", // 对应发票中的"规格型号"
            goodsUnit: "" // 单位
        }
    ]
}
```

