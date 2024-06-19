Table
A data table package which has following:

Pagination
Search filter for each column
Actions with View, Edit and Delete
Sort for each column
User should be able to enter values in the cells of the table.


Install

npm i smarttable



Import

import DataTableTest from 'smarttable';



Setup


 const data1 = [
      { id: 1, name: 'John Doe', age: 28, email: 'john@example.com' },
      { id: 2, name: 'Jane Doe', age: 22, email: 'jane@example.com' },
      { id: 3, name: 'Alice Smith', age: 34, email: 'alice@example.com' },
      { id: 4, name: 'Bob Johnson', age: 45, email: 'bob@example.com' },
      // Add more rows as needed
  ]
  const [data,setData] = useState(data1)

  const columns = useMemo(
    () => [
      {
        Header: 'Name',
        accessor: 'name',
        id: 'name',
      },
      {
        Header: 'Age',
        accessor: 'age',
        id: 'age',
      },
      {
        Header: 'Email',
        accessor: 'email',
        id: 'email',
      },
    ],
    []
  );

  const handleView = (row) => {
    alert(`Viewing row: ${JSON.stringify(row)}`);
  };

  const handleEdit = (row) => {
    alert(`Editing row: ${JSON.stringify(row)}`);
  };

  const handleDelete = (row) => {
    alert(`Deleting row: ${JSON.stringify(row)}`);
  };

<DataTableTest
        columns={columns}
        data={data}
        onView={handleView}
        onEdit={handleEdit}
        onDelete={handleDelete}
      />
    </div>
