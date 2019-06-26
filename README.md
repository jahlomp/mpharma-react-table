# mpharma-react-table

> A simple reusable table component in React

[![NPM](https://img.shields.io/npm/v/mpharma-react-table.svg)](https://www.npmjs.com/package/mpharma-react-table) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install git://github.com/chiamaka/mpharma-react-table.git#master
```

## Usage

```jsx
import React from 'react';
import Table from 'mpharma-react-table';

const headers = [
  { title: 'Name', align: 'left', dataIndex: 'name' },
  { title: 'Age', align: 'left', dataIndex: 'age' },
  { title: 'Country', align: 'left', dataIndex: 'country' }
];

const data = [
  {
    name: 'Chiamaka',
    age: 25,
    country: 'Nigeria'
  },
  {
    name: 'Nick',
    age: 30,
    country: 'Ghana'
  }
];

function Example() {
  return <Table headers={headers} data={data} />;
}
```

> (\*) means required

## API

Table - Default export (Top level) i.e `import Table from mpharma-react-table`

TableHeaders - Named export i.e. `import { TableHeaders } from mpharma-react-table`

## Table Props

| Name               | Type           | Default              | Description                                                                      |
| ------------------ | -------------- | -------------------- | -------------------------------------------------------------------------------- |
| \*headers          | array[objects] | None                 | The headers of the table. See Header props for more info                         |
| \*data             | array[objects] | None                 | Data to be rendered                                                              |
| renderIcon         | function       | None                 | Funtion which renders any icon passed into it. The icon can be a react component |
| tableStyle         | object         | None                 | Style for the table wrapper                                                      |
| rowsPerPageOptions | array[numbers] | [25, 50, 100]        | Customizes the options of the rows per page select field                         |
| hover              | bool           | false                | If true, the table row will shade on hover                                       |
| handleRowClick     | function       | () => {}             | Function to call when a row is clicked                                           |
| emptyMessage       | string         | 'No data available!' | Customizes the message when there is no data to display                          |
| emptyMessageStyle  | object         | None                 | Customizes the styling of the empty message                                      |

## Headers Props

| Name      | Type                          | Default                         | Description                                                                                     |
| --------- | ----------------------------- | ------------------------------- | ----------------------------------------------------------------------------------------------- |
| \*title   | string                        | None                            | Title of the header                                                                             |
| align     | string: (left, center, right) | left                            | How you want the header and the corresponding data to be aligned                                |
| dataIndex | string                        | None                            | Key that ties data to the header. Should be the key of the data that you want under this header |
| width     | number                        | inherit                         | Specify width for the header                                                                    |
| style     | object                        | { textTransform: 'capitalize' } | Specify the style for the column data                                                           |
|           |

## TableHeader Props

| Name      | Type           | Default | Description                                 |
| --------- | -------------- | ------- | ------------------------------------------- |
| \*headers | array[strings] | None    | The headers of the table                    |
| style     | object         | None    | Style object for the table header component |

## Contributing

1. clone the project and cd into project
2. npm install && npm start
3. create another terminal window and cd into example/ && npm start

## License

MIT © [chiamaka](https://github.com/chiamaka)
