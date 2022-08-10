### 剑指 Offer 43. 1～n 整数中 1 出现的次数
输入一个整数 n ，求1～n这n个整数的十进制表示中1出现的次数。

例如，输入12，1～12这些整数中包含1 的数字有1、10、11和12，1一共出现了5次。

### 示例 1：
    输入：n = 12
    输出：5

### 示例 2：
    输入：n = 13
    输出：6

### 思路:
    规律：9    -> 1     
         99   -> 20
         999  -> 300
         9999 -> 4000
    1的个数总和：最高位为1的个数 + 当前位数的值*(i*10的(i-1)次方) + dp[i-1]
    例如： 999 = [100-200]中 1 出现的次数 + ([200-300],[300-400],[400-500],[500-600],[600-700],[700-800],[800-900](每个区间1的个数都相等，所以计算一个*当前值)) + [0-99]中的个数(dp[i-1])

### 代码：
    var countDigitOne = function(n) {
        let arr = String(n).split('').reverse()
        let length = arr.length
        let dp = new Array(length)
        if(arr[0] == 0){
            console.log(1)
            dp[0] = 0
        }else{
            dp[0] = 1
        }
        for(let i = 1; i < length; i++){
            if(arr[i] == 0){
                dp[i] = dp[i - 1]
                continue
            }
            if(arr[i] == 1){
                dp[i] = +arr.slice(0, i).reverse().join('') + 1 + arr[i]*i*Math.pow(10, i - 1) + dp[i-1]
            }else{
                dp[i] = Math.pow(10, i) + arr[i]*i*Math.pow(10, i - 1) + dp[i-1]
            }
        }
        return dp[length - 1]
    };
