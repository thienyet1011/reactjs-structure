- Cấu trúc dự án, bao gồm:

1. build: Chứa các file sau khi chạy lệnh "npm run build" or "yarn build" để phục vụ cho việc deploy lên Production server
2. config: Chứa các thông số cấu hình của dự án như API_URL, PORT, ... 
    (Lưu ý: hông lưu các thông tin bảo mật như: PASSWORD, SECRET_KEY, ...)
3. mock: Chứa mock-up data chủ yếu là các file *.json, phục vụ cho việc giả lập dữ liệu, trong quá trình chờ phía Back-end 
    cung cấp API
4. store: Chứa file cấu hính liên qua đến Redux Store, Middlewares (redux-thunk, redũ-saga, redux-persist, redux-log, ...)
5. src: 
    5.1: common: Chứa các thông tin dùng chung cho toàn bộ dự án
        5.1.a: actions: Chứa các redux action dùng chung như USER_PROFILE, AUTH_TOKEN, LOGGED_IN_STATUS, ...
        5.1.b: assets: Chứa global CSS (SCSS, SASS, Less, ...)
        5.1.c: components:
            5.1.c-1: controls: Chứa các custom compoents liên quan đến tương tác với Form như Input, Button, Select, Textarea,...
            5.1.c-2: layout: Chứa các custom components liên quan đến layout như Navbar, Sidebar, Top Menu, Header, Footer, ,,,
            5.1.c-3: others: Chứa các custom compoents khác như Card, Label, Alert, Avatar, Dialog,....
        5.1.d: reducers: Chức các redux reducer (global state) dùng chung 
    5.2: modules: Chưa các chức năng chinh. Vd: Có các chức năng Auth, Home, About, Contat, Product,..
        Trong mỗi module cũng sẽ bao gồm các thư mục: actions, reducers, assets, components & pages. Vd module "Auth":
        5.2.a: Auth:
            5.2.a-1: actions
            5.2.a-2: assets
            5.2.a-3: components
                5.2.a-3.1: Login Form 
                5.2.a-3.2: Register Form 
                ...
            5.2.a-4: pages 
                5.2.a-4.1: Login page 
                5.2.a-4.2: Register page 
                5.2.a-4.3: Change password page 
            5.2.a-5: reducers
        5.2.b: Home
        5.2.c: Product
        5.2.d: About
        5.2.e: Contact
6. routes: Chức các file liên quan tới định nghĩa route (React-router-dom), custom routes (Private route, Lock route)
7. utils: Chứa các file tiện ích

