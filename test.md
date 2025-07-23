https://pbchain.hik-cloud.com/v1/siot/ar/textSearch/covertBigPic

https://pbchain.hik-cloud.com/v1/siot/ar/textSearch/downLoadBigPic

https://pbchain.hik-cloud.com/v1/siot/ar/textSearch/evaluate


```js
reOrganizationData (data) {
      const pIds = [
        ...new Set(data.map((item) => (item.pId === null ? item.id : item.pId)))
      ].map((item) => ({
        id: item,
        children: []
      }));
      if (pIds.length === data.length) return data;
      else {
        const result = data.reduce((prev, cur) => {
          const parentIndex = prev.findIndex((item) => item.id === cur.id);
          if (parentIndex !== -1) {
            prev[parentIndex] = {
              ...prev[parentIndex],
              ...cur
            };
          } else {
            const childrenIndex = prev.findIndex((item) => item.id === cur.pId);
            if (childrenIndex !== -1) prev[childrenIndex].children.push(cur);
          }
          return prev;
        }, pIds);
        return this.reOrganizationData(result);
      }
    },
```





https://acsc-pre.hikyun.com/mpvisitor/visitor/staff?sessionId=&isAllowLogin=1&menuList=null&reason=null&flag=1729477300000&invitation=false&cloudTalkToken=



https://hitom-dev2.hikyun.com/webapi/hatom/web/rest/v1/app/setInformation/android_com_ceshi_qwer304/

```json
《以父之名》、《夜的第七章》、《止战之殇》 pluginFramework

http://b2b.beingmate.com/personnel/checkSendSms.do
{"mobilephone":"Zj+4LwLZXU8T9CFWUmheYQ==","loginName":"5HcWrNT7du5utR9DGixYMw==","rsaKey":"lEAJK68kE4h61rJF3ku5jwfiTrzZlozGqYSs6SIhY2Glfhr7AHeBuSypBmBHZFIhKG77kmuzHqUAn3gQVd0yM/yjsQdZev6Eoo7vjOIOoMFZRCVN7pSrsKvuLNIgVXZJnH3i3rtplGPwc1Q3wtdkJXdc4m/AlHTFdUR9EfK6wEk="}

%Java_Home%\bin;
%Java_Home%\jre\bin;
C:\Program Files\Common Files\Oracle\Java\javapath;
%SystemRoot%\system32;
%SystemRoot%;%SystemRoot%\System32\Wbem;
%SYSTEMROOT%\System32\WindowsPowerShell\v1.0\;
%SYSTEMROOT%\System32\OpenSSH\;
C:\Program Files\TortoiseSVN\bin;D:\Yarn\bin\;
%NVM_HOME%;%NVM_SYMLINK%;
D:\nodejs\node_global;
E:\nvm\v17.6.0:\Tool\AdbTool\;
D:\wxTool\;
D:\Git\cmd;
D:\Subversion\bin;
D:\wxTool\dll;
D:\Python
```

#1196db

\#3379fd

https://10.1.77.77/USTA-rqm_swcus/branches/custom/IPM2022030701545呈贡雪亮小程序定制/rqm_swcus/miniprogram/rqm-community-mp

```javascript
Date.prototype.format = function (fmt) {
                const o = {
                  "M+": this.getMonth() + 1, // 月份
                  "d+": this.getDate(), // 日
                  "h+": this.getHours(), // 小时
                  "m+": this.getMinutes(), // 分
                  "s+": this.getSeconds(), // 秒
                  "q+": Math.floor((this.getMonth() + 3) / 3), // 季度
                  S: this.getMilliseconds() // 毫秒
                };
                if (/(y+)/.test(fmt)) {
                  fmt = fmt.replace(
                    RegExp.$1,
                    (this.getFullYear() + "").substr(4 - RegExp.$1.length)
                  );
                }
                for (const k in o) {
                  if (new RegExp("(" + k + ")").test(fmt)) {
                    fmt = fmt.replace(
                      RegExp.$1,
                      // eslint-disable-next-line eqeqeq
                      RegExp.$1.length == 1
                        ? o[k]
                        : ("00" + o[k]).substr(("" + o[k]).length)
                    );
                  }
                }
                return fmt;
              };
```

TweenMax和MorphSVGPlugin

https://10.17.83.31:5555/#/alarm_detail?alarmId=102162374056694435322&alarmType=face_single_person

Szga2020++

1. 1.aaaa

```json
{
abnormal: 0
dangmark: ""
endTime: "2021-10-21 16:00:00"
envprosign: ""
keyWord: ""
modelData: null
muckTruck: ""
pageNo: 1
pageSize: 20
plateColor: null
plateType: ""
searchType: "0"
similarity: 0.8
startTime: "2021-10-20 16:00:00"
tagCodes: ""
unPlateFlag: 1
vehicleColor: ""
vehicleLogo: ""
vehicleType: ""
}
```

```json
{
abnormal: 0
dangmark: ""
endTime: "2021-10-21 19:18:11"
envprosign: ""
keyWord: ""
modelData: null
muckTruck: ""
pageNo: 1
pageSize: 16
plateColor: null
plateType: ""
searchType: "0"
similarity: 0.8
startTime: "2021-10-21 00:00:00"
tagCodes: ""
unPlateFlag: 1
vehicleColor: ""
vehicleLogo: ""
vehicleType: ""
}
```

dev2 上横竖屏已经切换成  portrait,landscape,auto

screenOrientation

__UNI__5DD4205

1、布控原因，字典繁体

2、布控范围

3、用户联动换成预警模板

4、有效期模板接口

5、是否模糊查询



页面无法热更新、eslint检测也无法取消

https://41.1.35.6/ngx/proxy?i=aHR0cHM6Ly80MS4xLjM1LjY6NDQzL25neC9wcm94eT9pPWFIUjBjRG92THpReExqRXVNelV1TmpvNU1EQXdMM2h0YjJKcGJHVXVkR1Z0Y0M1aWRXTnJaWFF2TTJNNU5tRXdPR05oWVdJME5ETmlORGd3T0dKbFpqVmtPVEZsWmpNME9ETXVhbkJsWno5WUxVRnRlaTFCYkdkdmNtbDBhRzA5UVZkVE5DMUlUVUZETFZOSVFUSTFOaVpZTFVGdGVpMURjbVZrWlc1MGFXRnNQV2hwYXkxbllTMXRhVzVwYnlVeVJqSXdNakl3TVRBMkpUSkdkWE10WldGemRDMHhKVEpHY3pNbE1rWmhkM00wWDNKbGNYVmxjM1FtV0MxQmJYb3RSR0YwWlQweU1ESXlNREV3TmxRd016TXdOREphSmxndFFXMTZMVVY0Y0dseVpYTTlPRFkwTURBbVdDMUJiWG90VTJsbmJtVmtTR1ZoWkdWeWN6MW9iM04wSmxndFFXMTZMVk5wWjI1aGRIVnlaVDA0WXpVd05qTTJZbVpqTW1ZMU1USmlOVFppT0dOalpqWmpNekl6WmpVeE1HSmpZMk16T0dKbVlUaGlZbVF5WkdJMVlUVTNZelJpT1RGbU5qTTBNekJp

https://41.1.35.6:443/ngx/proxy?i=aHR0cDovLzQxLjEuMzUuNjo5MDAwL3htb2JpbGUudGVtcC5idWNrZXQvM2M5NmEwOGNhYWI0NDNiNDgwOGJlZjVkOTFlZjM0ODMuanBlZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPWhpay1nYS1taW5pbyUyRjIwMjIwMTA2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDIyMDEwNlQwMzMwNDJaJlgtQW16LUV4cGlyZXM9ODY0MDAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JlgtQW16LVNpZ25hdHVyZT04YzUwNjM2YmZjMmY1MTJiNTZiOGNjZjZjMzIzZjUxMGJjY2MzOGJmYThiYmQyZGI1YTU3YzRiOTFmNjM0MzBi

http://41.1.35.206:6501/pic?FA01603E0060F2040204*hcs07eb4b3cdaa8403b92020/vehiclebkg/12668;164205516174610334441064?pic*113090862*11500*18799*FA01603E0060F2040204-2*1642057380

```json
{
    "pageNo": 1,
    "pageSize": 20,
    "data": {
        "userId": "admin",
        "plateNo": "浙A",
        "excludePlateNo": false,
        "beginTime": "2022-06-09 00:00:00",
        "endTime": "2022-07-09 00:00:00",
        "vehicleColor": [],
        "plateColor": [],
        "vehicleType": [],
        "plateType": [],
        "orgCheck": [],
        "hasLinkFaceVehicle": "",
        "laneNo": "",
        "directionIndex": "",
        "hasPlateOrNot": "noLimits",
        "startTimeInterval": "",
        "endTimeInterval": "",
        "areaCodes": [],
        "crossingIds": []
    }
}

		"userId": "admin",
		"plateNo": "浙A",
		"excludePlateNo": false,
		"beginTime": "2022-06-28 00:00:00",
		"endTime": "2022-07-04 23:59:59",
		"vehicleColor": [],
		"plateColor": [],
		"vehicleType": [],
		"plateType": [],
		"orgCheck": [],
		"hasLinkFaceVehicle": "",
		"laneNo": "",
		"directionIndex": "",
		"hasPlateOrNot": "noLimits",
		"startTimeInterval": "",
		"endTimeInterval": "",
		"areaCodes": [],
		"crossingIds": []
```















