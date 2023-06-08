可以使用 JavaScript 的 Date 对象来实现时间转换的功能。下面是一个将时间戳转换成特定格式的函数示例。

```
function formatTimestamp(timestamp, format) {
  const date = new Date(timestamp);
  let year = date.getFullYear();
  let month = date.getMonth() + 1;
  let day = date.getDate();
  let hour = date.getHours();
  let minute = date.getMinutes();
  let second = date.getSeconds();

  // 格式化
  format = format.replace(/yyyy/g, year);
  format = format.replace(/MM/g, month.toString().padStart(2, '0'));
  format = format.replace(/dd/g, day.toString().padStart(2, '0'));
  format = format.replace(/HH/g, hour.toString().padStart(2, '0'));
  format = format.replace(/mm/g, minute.toString().padStart(2, '0'));
  format = format.replace(/ss/g, second.toString().padStart(2, '0'));
  return format;
}

// 用法示例
const timestamp = Date.now();
const formattedTime = formatTimestamp(timestamp, 'yyyy-MM-dd HH:mm:ss');
console.log(formattedTime); // 例如："2023-06-08 08:30:45"
```

这个函数中的`formatTimestamp`通过传入的时间戳以及格式，使用`Date`对象提取出日期、小时、分钟和秒数，并替换相应的格式符（如`yyyy`、`MM`、`dd`等），生成最终的格式化时间字符串。
