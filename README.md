[# markdown](https://www.markdownguide.org/basic-syntax/)

I. Cấu trúc dự án, bao gồm:
---------------------------

1. build: Chứa các file sau khi chạy lệnh "npm run build" or "yarn build" để phục vụ cho việc deploy lên Production server

2. config: Chứa các thông số cấu hình của dự án như API_URL, PORT, ... 

    > (Lưu ý: hông lưu các thông tin bảo mật như: PASSWORD, SECRET_KEY, ...)

3. mock: Chứa mock-up data chủ yếu là các file *.json, phục vụ cho việc giả lập dữ liệu, trong quá trình chờ phía Back-end cung cấp API

4. store: Chứa file cấu hính liên qua đến Redux Store, Middlewares (redux-thunk, redũ-saga, redux-persist, redux-log, ...)

5. src: 
    - apis: Chứa các file gọi api 

    - common: Chứa các thông tin dùng chung cho toàn bộ dự án

      1. actions: Chứa các redux action dùng chung như USER_PROFILE, AUTH_TOKEN, LOGGED_IN_STATUS, ...
      2. assets: Chứa global CSS (SCSS, SASS, Less, ...)
      3. components:
          + controls: Chứa các custom compoents liên quan đến tương tác với Form như Input, Button, Select, Textarea,...
          + layout: Chứa các custom components liên quan đến layout như Navbar, Sidebar, Top Menu, Header, Footer, ...
          + others: Chứa các custom compoents khác như Card, Label, Alert, Avatar, Dialog,....
      4. reducers: Chức các redux reducer (global state) dùng chung.

    - modules: Chưa các chức năng chinh. Vd: Có các chức năng Auth, Home, About, Contat, Product,..
        Trong mỗi module cũng sẽ bao gồm các thư mục: actions, reducers, assets, components & pages. Vd module "Auth":

        1. Auth:
            - actions
            - assets
            - components
                + Login Form 
                + Register Form 
                + ...
            - pages 
                + Login page 
                + Register page 
                + ... 
            - reducers
        2. Home
        3. ...

    - routes: Chức các file liên quan tới định nghĩa route (React-router-dom), custom routes (Private route, Lock route)

    - utils: Chứa các file tiện ích
----
II.  Tên file: 
---------------------------
1. src 
    - component 
        - global => ```C{ten(file}```
        - local => ```M{ten_file}```
    - redux 
        - global
            - action => ```{ten_action}.action.js```. VD: login.action.js
            - reducer => ```reducer.js``` <=> combine của các reducer con trong global
        - local 
            - acton => ```{ten_module}.{ten_action}.action.js```. VD: auth.login.js
            - reducer => ```{ten_module}.reducer.js``` <=> combine của các reducer con. VD: auth.reducer.js