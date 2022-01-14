### 1078. Bigram 分词
给出第一个词first 和第二个词second，考虑在某些文本text中可能以 "first second third" 形式出现的情况，其中second紧随first出现，third紧随second出现。

对于每种这样的情况，将第三个词 "third" 添加到答案中，并返回答案。

### 示例 1：
    输入：text = "alice is a good girl she is a good student", first = "a", second = "good"
    输出：["girl","student"]

### 示例 2：
    输入：text = "we will we will rock you", first = "we", second = "will"
    输出：["we","rock"]

### 思路：
    把字符串按空格切割为单词数组然后遍历数组，满足条件就加入新数组，最后返回新数组

### 代码：
    var findOcurrences = function(text, first, second) {
        let arr = text.split(' ')
        let rel = []
        for(let i = 0; i < arr.length; i++){
            if(arr[i] == first && arr[i + 1] == second && i + 2 < arr.length){
                rel.push(arr[i + 2])
            }
        }
        return rel
    };
