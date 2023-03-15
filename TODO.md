1. 并发限制库：https://github.com/sourcegraph/conc  、 https://mp.weixin.qq.com/s/59cxPFHWcdnUxKyRyo8SKw

2. excel库提pr:  int获取cell字母
   ```go
   func (biAbTestingLogic) getCellIndexByNumber(number int) string {
   	mod := number % 26      // 取模
   	quotient := number / 26 // 取商
   	if quotient == 0 {
   		return string(rune('A' + mod))
   	}
   
   	return string(rune('A'+quotient-1)) + string(rune('A'+mod))
   }
   
   ```

   ```go
   func ColumnNumberToName(num int) (string, error) {
   	if num < MinColumns || num > MaxColumns {
   		return "", ErrColumnNumber
   	}
   	var col string
   	for num > 0 {
   		col = string(rune((num-1)%26+65)) + col
   		num = (num - 1) / 26
   	}
   	return col, nil
   }
   ```

   

3. 标准库https://books.studygolang.com/The-Golang-Standard-Library-by-Example/chapter01/01.0.html

4. 【前言】好气go为什么不是c语言    go语言自举https://www.zhihu.com/question/66944175

5. 编译第一课  源码
