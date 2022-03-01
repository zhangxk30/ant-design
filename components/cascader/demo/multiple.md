---
order: 5.1
version: 4.17.0
title:
  zh-CN: 多选
  en-US: Multiple
---

## zh-CN

一次性选择多个选项。

## en-US

Select multiple options

```jsx
import { Cascader } from 'antd';

const options = [
  {
    label: 'Light',
    value: 'light',
    children: new Array(20)
      .fill(null)
      .map((_, index) => ({ label: `Number ${index}`, value: index })),
  },
  {
    label: '广州',
    value: '广州',
    children: [
      {
        label: 'Little',
        value: 'little',
        children: [
          {
            label: '广州一区',
            value: '广州一区',
          },
          {
            label: '广州二区',
            value: '广州二区',
          },
          {
            label: '广州三区',
            value: '广州三区',
          },
        ],
      },
    ],
  },
];

const App = () => {
  const onChange = value => {
    console.log(value);
  };
  return (
    <Cascader
      style={{ width: '100%' }}
      options={options}
      onChange={onChange}
      multiple
      maxTagCount="responsive"
    />
  );
};

ReactDOM.render(<App />, mountNode);
```
