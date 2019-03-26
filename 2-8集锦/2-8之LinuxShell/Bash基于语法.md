# Bash基本语法

## 命令替换

使用``或者$()在bash中来捕获执行的命令的结果.

```
files=`ls` # files=$(ls)
echo $files
```

## if

```
if [ <test> ]; then
  ...
elif [ <test> ]; then
  ...
else
  ...
fi
```

### 整数测试

- `[ num1 -gt num2 ]`, >
- `-ge`, >=
- `-lt`, <
- `-le`, <=
- `-ne`, !=
- `-eq`, ==

```
if [ 2 -gt 1 ];then
  echo 'greater'
else
  echo 'lesser'
fi
```

### 字符测试

- `[[ value =~ pattern ]]`, 左边的值能够被右边的pattern正则匹配, pattern如果包含`\`, 则匹配会失败, 需要保存到变量, 然后引入进来.
- `value1 = value2`, 字符串相等为真
- `value1 != value2`, 字符串不相等为真
- `-z value`, 字符串为null则为真
- `-n value`, 字符串为null则为假

```
if [ 'str' = 'str' ];then
  echo 'equal'
fi
```

```
reg='^\w+$'
if [[ "adf123" =~ $reg ]]; then
  echo 'matched'
else
  echo 'not matched';
fi
```

### 文件测试

- `-d`, 目录是否存在
- `-f`, 文件是否存在

## 循环语句

### for

#### 可以对**空格或者换行符**分割的字符串进行循环

```
words="apple meat sleep woman"
for word in ${words}
do
 echo $word
done
```

#### 使用**{<start>..<end>..<step>}**来表示**ASCII字符**的范围值, 对**范围值**进行迭代

- 数字迭代, 例如{1..100}, {1..100..1}
- 字母迭代, 例如{a..z}, {Z..A}

```
for value in {0..100..5}
do
  echo $value
done
```

#### C风格循环

```
for((i=0;i<=100;i+=5))
do
  echo $i
done
```
