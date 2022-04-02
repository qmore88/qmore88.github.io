#Python Notes

####檔案路徑定義 (使用"/"作為路徑)
在 Windows 作業系統下指定檔案路徑時，爲了避免反斜線符號()被誤認成跳脫字元，你應該使用 Python 的原始字串，在字串的前面加上 r，或是在字串内容所有的反斜線前面加上另一個反斜線，像是：C:\\path\\to\\file.xlsx。

###全域變數
1. 只要在最上層有定義變數, 該變數就為全域變數
2. function 內會去往上層尋找變數名稱, 若上層有該變數, 則就會使用該變數
3. 若在function內要宣告全域變數, 需使用global關鍵
```python
def myprint():
    global s
    s = 'hello world'
    print('myprint: ' + s)
    myprint()
    print(s)
```
輸出結果為
```python
myprint: hello world
hello world
```


