JOSN 中带有中文时，为输出中文

```
with open('data.josn','w',encoding='utf-8') as file:
    	file.write(json.dumps(data,indent=2,ensure_ascii=False))
```

