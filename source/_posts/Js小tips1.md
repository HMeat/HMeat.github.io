# 对象.与对象[]  
声明一个对象属性与属性之间使用逗号分隔，属性与值之间使用冒号，例如：
```
  const animalgroup = {
    sheep: '喜羊羊',
    pig: '猪猪侠',
    horse: '彩虹马',
    1: '东海龙王'
  }
```
## 对象的调用
1、对象.key
```
  console.log(animalgroup.sheep); // 喜羊羊
```
2、对象[]
```
  const animal = 'pig'
  console.log(animalgroup[animal]); // 猪猪侠
```
```
  console.log(animalgroup["horse"]);  // 彩虹马
```
## 对象的新增、修改
1、对象.属性名 = 属性值 
如果存在则修改，如果不存在则新增。  
**新增**
```
  animalgroup.snake = '小青'
  console.log(animalgroup);
  // {1: '东海龙王', sheep: '喜羊羊', pig: '猪猪侠', horse: '彩虹马', snake: '小青'}
```
**修改**
```
  animalgroup.sheep = '懒洋洋'
  console.log(animalgroup);
  // {1: '东海龙王', sheep: '懒洋洋', pig: '猪猪侠', horse: '彩虹马'}
```
2、对象[属性名] = 属性值  
**新增**
```
  animalgroup["mouse"] = '杰瑞'
  console.log(animalgroup);
  // {1: '东海龙王', sheep: '喜羊羊', pig: '猪猪侠', horse: '彩虹马', mouse: '杰瑞'}
```
**修改**
```
  animalgroup["horse"] = '小白马'
  console.log(animalgroup);
  // {1: '东海龙王', sheep: '喜羊羊', pig: '猪猪侠', horse: '小白马'}
```
## 对象.与对象[]区分
1、对象[]用于获取动态key的value值
2、对象[]可以拿到数字形式key的值，对象.数字值的key会报错
```
 console.log(animalgroup[1]);  // 东海龙王
```
3、对象.可以将关键字作为属性名进行添加，对象[]会抛出异常
```
  animalgroup.let = "你好"
  // {1: '东海龙王', sheep: '喜羊羊', pig: '猪猪侠', horse: '彩虹马', let: '你好'}
  animalgroup[let] = "世界" 
  // a.html:63 Uncaught ReferenceError: let is not defined
```
4、对象.不能调用字符串变量，对象[]可以
```
  const animal = 'pig'
  console.log(animalgroup[animal]); // 猪猪侠
```
```
  const animal = 'pig'
  console.log(animalgroup.animal);  // undefined
```
## 返回数组形式的对象名
```
  console.log(Object.keys(animalgroup));
  // ['1', 'sheep', 'pig', 'horse']
```
## 删除对象属性
```
  delete animalgroup[1]
  console.log(animalgroup);
```
## 判断对象是否包含属性
```
  console.log("horse" in animalgroup);  // true
  console.log(2 in animalgroup);  // false
```
## 遍历对象
```
  for (const key in animalgroup) {
    if (key.length > 2) {
      console.log(key);
    }
  }
```
![image](https://github.com/HMeat/HMeat.github.io/assets/136236305/fe6762d3-d29f-4fa8-98cd-e0f5640fb708)
