## 安裝Dash

Dash 是建構於 Plotly.js、React.js 與 Flask 之上的 Python 網頁應用程式框架，能夠將常見的使用者介面元件包含像是下拉式選單、滑桿或圖形與 資料分析應用快速地連結起來，讓以 Python 為主的資料科學團隊不需要 JavaScript 也可以建立出具備高度互動性的圖表與儀表板。<br>

dash_core_components 與 dash_html_components組件庫包含了一系列Pythoon版本的HTML標籤。其中 dash_core_component 這種交互式高階組件庫使用的並非僅有HTML語言，而是包含JavaScript、HTML和CSS，並由React.js庫生成的。<br><br>

在終端機執行
```
pip install dash
pip install dash-html-components
pip install dash-core-components
```


### 使用Dash製作HTML

Dash是由兩個部分所組成的，分別是Layout及Callback。前者是網頁應用程式的樣式設計(外觀)，後者為應用程式的互動。

```
import dash
import dash_core_components as dcc
import dash_html_components as html

app = dash.Dash()
app.layout = html.Div(children=[
html.H1(children='你好，Dash'),
html.Div(children='''
Dash: Python網絡應用框架'''),
dcc.Graph(
id='example-graph',
figure={
'data': [
{'x': [1, 2, 3], 'y': [4, 1, 2], 'type': 'bar', 'name': '北京'},
{'x': [1, 2, 3], 'y': [2, 4, 5], 'type': 'bar', 'name': '天津'},
],
'layout': {
'title': 'Dash數據可視化'
}
}
)
])
if __name__ == '__main__':
app.run_server(debug=True)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/YuTe-Lai/yute-dash.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
