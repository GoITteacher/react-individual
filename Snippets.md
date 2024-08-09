```json
{
  "Redux Slice Template": {
    "prefix": "redux-slice",
    "body": [
      "import { createSlice } from \"@reduxjs/toolkit\";",
      "const initialState = ${1:{}};",
      "",
      "export const ${2:sliceName} = createSlice({",
      "  name: \"${3:name}\",",
      "  initialState,",
      "  reducers: {",
      "    ${4:reducer1}(state, action) {},",
      "    ${5:reducer2}(state, action) {},",
      "    ${6:reducer3}(state, action) {},",
      "    ${7:customReducer}: {",
      "      reducer(state, action) {},",
      "      prepare(${8:userData}) {},",
      "    },",
      "  },",
      "});",
      "",
      "export const { ${9:name} } = ${2:sliceName}.actions;",
      "export default ${2:sliceName}.reducer;"
    ],
    "description": "Template for creating a Redux slice using createSlice from @reduxjs/toolkit"
  },

  "React-Redux Configure Store": {
    "prefix": "react-configure-store",
    "body": [
      "import { configureStore } from \"@reduxjs/toolkit\";",
      "import reducer from \"location\";",

      "export default configureStore({",
      "  reducerName: reducer,",
      "  reducerName: reducer,",
      "  reducerName: reducer,",
      "});"
    ],
    "description": "React Configure Store"
  },

  "React Fetch GET Axios": {
    "prefix": "react-api-get",
    "body": [
      "export const fetchGet = createAsyncThunk(\"name/fetchName\",",
      "async (_, thunkAPI) => {",
      "   const BASE_URL = \"\";",
      "   const END_POINT = \"\";",
      "   const url = BASE_URL + END_POINT;",
      "",
      "   const params = {};",
      "   const headers = {};",
      "",
      "   try {",
      "     const response = await axios.get(url, { params, headers });",
      "     return response.data;",
      "   } catch (e) {",
      "     return thunkAPI.rejectWithValue(e.message);",
      "   }",
      "}",
      ");"
    ],
    "description": "Create Axios Fetch (GET) Function"
  },

  "React Fetch POST Axios": {
    "prefix": "react-api-post",
    "body": [
      "export const fetchPost = createAsyncThunk(",
      "'tasks/fetchAll',",
      "async (userData, thunkAPI) => {",
      "   const BASE_URL = '';",
      "   const END_POINT = '';",
      "   const url = BASE_URL + END_POINT;",
      "   const params = {};",
      "   const headers = {};",
      "   try {",
      "   const response = await axios.post(url, userData, { params, headers });",
      "   return response.data;",
      "   } catch (e) {",
      "   return thunkAPI.rejectWithValue(e.message);",
      "   }",
      "},",
      ");"
    ],
    "description": "Create Axios Fetch (POST) Function"
  },

  "Lazy Loaded Routes with Suspense": {
    "prefix": "lazy-suspense-routes",
    "body": [
      "const MyComponent = lazy(() => import('${1:path/to/MyComponent}'));",
      "<Suspense fallback={<div>Loading...</div>}>",
      "  <Routes>",
      "    <Route path=\"/path1\" element={<MyComponent />} />",
      "    <Route path=\"/path2\" element={<MyComponent />}>",
      "      <Route path=\"pathin1\" element={<MyComponent />} />",
      "      <Route path=\"pathin2\" element={<MyComponent />} />",
      "      <Route path=\"pathin3\" element={<MyComponent />} />",
      "    </Route>",
      "    <Route path=\"/path3\" element={<MyComponent />} />",
      "    <Route path=\"/path4\" element={<MyComponent />} />",
      "  </Routes>",
      "</Suspense>"
    ],
    "description": "Lazy Loaded Routes with Suspense in React"
  },

  "React Extra Reducer": {
    "prefix": "react-extra-reducer",
    "body": [
      "extraReducers: builder => {",
      "   builder",
      "     .addCase(fetchCategories.fulfilled, (state, action) => {",
      "       state.isLoading = false;",
      "       state.error = null;",
      "       state.items = action.payload;",
      "     })",
      "     .addCase(fetchCategories.pending, handlePending)",
      "     .addCase(fetchCategories.rejected, handleRejected);",
      "},"
    ],
    "description": "Create React Extra Reducer For Async Redux"
  },

  "React Array Render": {
    "prefix": "react-array-render",
    "body": [
      "<ul>{array.map((item) => {",
      "   return <li key={item.id}>",
      "      <UserElement data={item}/>",
      "   </li>",
      "})}</ul>;"
    ],
    "description": "Create Render Array"
  },

  "React Fetch In Component": {
    "prefix": "react-fetch-effect",
    "body": [
      "useEffect(() => {",
      "   async function fetchData() {",
      "      const data = await myFetchFunction();",
      "      setData(data);",
      "   }",
      "   ",
      "   fetchData();",
      "}, []);"
    ],
    "description": "Create "
  },

  "React Functional Component": {
    "prefix": "rfc",
    "body": [
      "import PropTypes from 'prop-types';",
      "import \"./${TM_DIRECTORY/(.*\\/)?([^\\/]+)$/${2:/pascalcase}/}.css\";",
      "import style from \"./${TM_DIRECTORY/(.*\\/)?([^\\/]+)$/${2:/pascalcase}/}.module.css\";",
      "import {useState} from \"react\"",
      "",
      "const ${TM_DIRECTORY/(.*\\/)?([^\\/]+)$/${2:/pascalcase}/} = ({}) => {",
      "  return (",
      "    <div>",
      "      ${TM_DIRECTORY/(.*\\/)?([^\\/]+)$/${2:/pascalcase}/}",
      "    </div>",
      "  )",
      "};",
      "",
      "export default ${TM_DIRECTORY/(.*\\/)?([^\\/]+)$/${2:/pascalcase}/};",
      "",
      "${TM_DIRECTORY/(.*\\/)?([^\\/]+)$/${2:/pascalcase}/}.propTypes = {",
      "  props1: PropTypes.string,",
      "  props2: PropTypes.string.isRequired,",
      "  props3: PropTypes.number.isRequired,",
      "};"
    ],
    "description": "React Functional Component"
  },

  "Use Dispatch with useEffect": {
    "prefix": "redux-async-dispatch",
    "body": [
      "import { useDispatch } from 'react-redux';",
      "import { ${1:action} } from '${2:../../..action.js}';",
      "import { useEffect } from 'react';",
      "",
      "const dispatch = useDispatch();",
      "useEffect(() => {",
      "  dispatch(${1:action}(${3:someData}));",
      "}, [${4:}]);"
    ],
    "description": "Use dispatch with useEffect in React"
  }
}
```
