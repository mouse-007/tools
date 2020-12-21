# 从query字符串中提取参数的值

```
/**
 * 从query字符串中提取参数的值
 * @param {*} str query字符串
 * @param {*} key 目标
 */
function getSearchParams(str, key){
  if(!str || !key || typeof str !== 'string' || typeof key !== 'string')return '';
  const reg = new RegExp(`[^?&]*${key}\\=[^&]+`, "g");
  let arr = str.match(reg)
  if(!arr)return "";
  arr=arr.map(n => n.replace(`${key}=`, ""));
  if (arr.length===0)return '';
  if (arr.length === 1) return arr[0];
  return arr;
}

// 例子
const str = "http://www.abc.com/index.html?a=6&b=2&c=3&c=6&c=7";
// 获取a
getSearchParams(str, 'a')  // 输出 6 (string)
// 获取f
getSearchParams(str, 'f')  // 输出 ''
// 获取c
getSearchParams(str, 'c')  // 输出 [3, 6, 7] (array)
```
