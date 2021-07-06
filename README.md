# 模型使用说明

[github地址](https://github.com/Lame-Unicorn/Models)

## 图片标注（Caption.py）

~~~python
def initialize(debug=False):
    """
    加载模型。
    必须在预测和释放操作之前执行。

    Parameters
    ----------
    debug: bool, default False
        debug 模式下将提供阶段性输出来提示模型的加载和预测情况并将预测结果转换成句子。

    """
~~~

```python
def release():
    """
    释放模型。
    只能在加载模型之后执行。
    """
```

```python
def predict(img):
    """
    预测图片内容。
    只能在加载模型后且未释放模型时执行。

    Parameters
    ----------
    img: str
        图片的绝对路径。

    Returns
    -------
    list or str
        返回形状为 (1, length) 的列表，列表元素为单词的索引值。
        debug 模式下，返回预测句子字符串。
        若产生异常，返回以 E: 开头的异常字符串。
    """
```

