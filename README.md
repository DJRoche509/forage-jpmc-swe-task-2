# JPMorgan Chase Software Engineering Virtual Experience - Task 2

Welcome to Task 2 of the JPMorgan Chase Software Engineering Virtual Experience! This task is about enhancing the client-side web application to display a continuously updating line graph based on stock data received from the server application. Issues related to duplicate data were addressed and the correct display of the graph was ensured. 

## Task Overview
### Purpose
The objective of this task is to fix the client-side web application so that it displays a graph that automatically updates as it receives continuous data from the server application. The graph should represent stock prices, with the y-axis indicating the stock’s top_ask_price and the x-axis representing the timestamp of the stock. Additionally, responsibility for aggregating duplicate data retrieved from the server should be assumed.

### Acceptance Criteria
This task is considered complete when the client-side web application displays a continuously updating line graph. The y-axis should represent the stock’s top_ask_price, and the x-axis should represent the timestamp of the stock. The graph should continuously update as a result of continuous requests and responses to and from the server for stock data. Moreover, the application should be able to aggregate duplicated data received from the server.

## Steps Completed
### 1. Setting Up the Local Development Environment
- Fork and clone the project repository from [GitHub](https://github.com/theforage/forage-jpmc-swe-task-2).
- Install necessary tools and dependencies using npm:
  ```
  npm install
  ```
### 2. Fixing the Client-Side Web Application
- Run the server file to establish a connection:
  ```
  python datafeed/server3.py
  ```
-  Start the client-side application to visualize the stock data:
  ```
  npm start
  ```
-  Made adjustments to the TypeScript files in the repository to ensure the correct functioning of the web application.
-  Modified the class constructor and `getDataFromServer()` method in `App.tsx` to display a continuous data feed.
-  Re-implemented the `componentDidMount()` method in `Graph.tsx` to properly render and react to state changes, ensuring the Graph component updates dynamically.
-  Enabled `PerspectiveViewerElement` to behave like an HTMLElement by extending the `HTMLElement` interface. Additional attributes such as `view`, `column-pivots`, `row-pivots`, `columns`, and `aggregates` were added to the element.'
    <br/><br/><br/><br/>
    As a result, this visual and dynamic graph below was created with streaming data upon the click of the blue "Start Streaming Data" button. <br/><br/>
    ![image](https://github.com/DJRoche509/forage-jpmc-swe-task-2/assets/100164051/3b4374f6-5c20-4600-9424-02b98e7cedf1)

  
### 3. Generating a Patch File
- Generate a patch file to record the changes made after the committed code was pushed to the remote repository:
  ```
  git format-patch -3 --stdout > task2_changes.patch
  ```

## Dependencies
- @finos/perspective: ^1.6.2
- @finos/perspective-viewer: ^1.6.2
- @finos/perspective-viewer-d3fc: ^1.6.2
- @finos/perspective-viewer-datagrid: ^1.6.2
- @types/jest: ^23.3.13
- @types/node: ^10.12.19
- @types/react: ^16.9.0
- @types/react-dom: ^16.0.11
- bootstrap: ^4.2.1
- puppeteer: ^1.19.0
- react: ^16.9.0
- react-dom: ^16.9.0
- react-scripts: 2.1.3
- awesome-typescript-loader: ^5.2.1
- source-map-loader: ^0.2.4
- typescript: ^3.2.4
  
