# Hướng dẫn

## 1. Tạo file .env trong folder api

- Mở file .env.example lên để tham khảo các variable

- HOST: mặc định là `localhost`
- PORT: mặc định là `4000`
- PRODUCTION_HOST: URL khi deploy, phục vụ cho convert link image product trên production khi build
- SECRET_KEY_JWT: key cho JWT
- DB_URL: URL dẫn đến database

## 2. Run server

Đầu tiên cần `cd api` để vào thư mục api.

- `yarn start`: Chạy server ở chế độ typescript
- `yarn build`: Build server từ ts -> js
- `yarn prod`: Build server từ ts -> js và run ở chế độ production

## 3. Kiểm tra

Kiểm tra server tại `localhost:4000`

## 4. Một số lưu ý

- Việc tạo sản phẩm phải qua 2 bước:

1. Up ảnh lên server -> server trả về name string của ảnh
2. Bỏ name string vào thuộc tính image trong body để add sản phẩm
3. Server sẽ tự tính và trả về đường link ảnh đầy đủ dựa vào môi trường development hay production
