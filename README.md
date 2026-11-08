# Thửa đất Bắc Ninh – MCP

Kết nối trợ lý AI (Claude, ChatGPT, Cursor…) với dữ liệu thửa đất tại Bắc Ninh trên [BumiAtlas](https://bumiatlas.com) qua Model Context Protocol (MCP).

- Tra cứu thửa đất theo số tờ bản đồ và số thửa như ghi trên sổ đỏ, sổ hồng (*"tờ 7 thửa 34, Đông Ngàn, Từ Sơn"*), theo mã thửa đất hoặc theo tọa độ
- Mục đích sử dụng đất (ODT đất ở đô thị, ONT đất ở nông thôn, LUC đất chuyên trồng lúa, CLN đất trồng cây lâu năm…), diện tích ghi nhận và diện tích theo ranh thửa
- Địa chỉ theo đơn vị hành chính mới (từ 1/7/2025) và địa chỉ cũ (phường, xã, quận, huyện) như trên giấy chứng nhận cấp trước đó; tìm bằng tên cũ hay tên mới, có dấu hoặc không dấu
- Ảnh vệ tinh hoặc bản đồ của thửa đất và các thửa xung quanh, mỗi thửa ghi số thửa

Từ 1/7/2025, tỉnh Bắc Ninh gồm cả tỉnh Bắc Giang cũ; dữ liệu phủ cả hai.

Dữ liệu là những gì các cổng thông tin công bố, nên chưa có đủ mọi thửa đất. Không có tên chủ sở hữu, số giấy chứng nhận hay giá đất.

## Kết nối

```
https://bumiatlas.com/mcp/bacninh
```

Thêm địa chỉ này làm custom connector (trình kết nối tùy chỉnh) trong Claude, ChatGPT, Cursor hoặc ứng dụng khác hỗ trợ MCP, rồi đăng nhập bằng Google. Không cần API key. Hướng dẫn chi tiết: [bumiatlas.com/mcp-docs/bacninh](https://bumiatlas.com/mcp-docs/bacninh).

Tên công cụ bằng tiếng Anh, nhưng trợ lý vẫn trả lời bằng tiếng Việt. Đây là bộ công cụ Việt Nam của BumiAtlas, nên cũng tra cứu được thửa đất ở các tỉnh, thành khác.

## Công cụ

| Công cụ | Chức năng |
|---|---|
| `VN_parcel_search` | Tìm thửa đất theo mã thửa, theo số tờ và số thửa kèm địa danh, hoặc theo tọa độ `vĩ độ, kinh độ` |
| `VN_parcel_get` | Chi tiết một thửa: mục đích sử dụng, diện tích, địa chỉ mới và cũ, các khu quy hoạch phủ lên thửa; ranh thửa dạng GeoJSON |
| `VN_parcel_image` | Ảnh vệ tinh hoặc bản đồ quanh một thửa hay một điểm; các thửa trong khung hình được viền và ghi số thửa |
| `VN_zoning_get` | Khu quy hoạch tại một điểm (TP. Hồ Chí Minh và Đà Nẵng): cấp quy hoạch, chức năng sử dụng đất, mật độ xây dựng, hệ số sử dụng đất, tầng cao |

## Ví dụ câu hỏi

- *"Tìm thửa đất tờ 7 thửa 34, phường Đông Ngàn, Từ Sơn."*
- *"Thửa đất tại 21.18452, 106.06861 ở TP. Bắc Ninh cũ là thửa nào?"*
- *"Tìm tờ 11 thửa 273, phường Hoàng Văn Thụ, TP. Bắc Giang."*

## Nguồn dữ liệu

Thửa đất từ guland.vn. Mỗi thửa ghi rõ nguồn.

## Các xã, phường có dữ liệu

Xếp theo quận, huyện, thị xã, thành phố cũ. Mỗi xã, phường mới (từ 1/7/2025) kèm các phường, xã, thị trấn cũ đã nhập vào.

### Bắc Ninh cũ

#### Huyện Gia Bình

- **Xã Cao Đức**: Cao Đức; Đức Long (Thị xã Quế Võ) _(phần lớn chưa có mục đích sử dụng đất)_
- **Xã Đông Cứu**: Giang Sơn, Song Giang _(phần lớn chưa có mục đích sử dụng đất)_
- **Xã Nhân Thắng**: Bình Dương, Nhân Thắng _(phần lớn chưa có mục đích sử dụng đất)_

#### Huyện Tiên Du

- **Xã Đại Đồng**: Hoàn Sơn, Đại Đồng, Tri Phương
- **Xã Liên Bão**: Liên Bão, Việt Đoàn, Hiên Vân
- **Xã Phật Tích**: Phật Tích, Cảnh Hưng
- **Xã Tân Chi**: Lạc Vệ, Tân Chi
- **Xã Tiên Du**: Phú Lâm, Nội Duệ, Lim

#### Huyện Yên Phong

- **Xã Tam Đa**: Thụy Hòa, Tam Đa, Đông Phong
- **Xã Tam Giang**: Tam Giang, Hòa Tiến
- **Xã Văn Môn**: Yên Phụ, Văn Môn, Đông Thọ
- **Xã Yên Phong**: Chờ, Trung Nghĩa, Đông Tiến, Long Châu
- **Xã Yên Trung**: Yên Trung, Dũng Liệt

#### Thành phố Bắc Ninh

- **Phường Hạp Lĩnh**: Hạp Lĩnh, Khắc Niệm
- **Phường Kinh Bắc**: Kinh Bắc, Hòa Long, Tiền Ninh Vệ, Suối Hoa, Khúc Xuyên
- **Phường Nam Sơn**: Nam Sơn, Vân Dương
- **Phường Võ Cường**: Võ Cường, Phong Khê, Đại Phúc
- **Phường Vũ Ninh**: Kim Chân, Thị Cầu, Đáp Cầu

#### Thành phố Từ Sơn

- **Phường Đồng Nguyên**: Đồng Nguyên, Đồng Kỵ, Trang Hạ
- **Phường Phù Khê**: Hương Mạc, Châu Khê, Phù Khê
- **Phường Tam Sơn**: Tam Sơn, Tương Giang
- **Phường Từ Sơn**: Đình Bảng, Tân Hồng, Phù Chẩn, Đông Ngàn

#### Thị xã Quế Võ

- **Phường Bồng Lai**: Mộ Đạo, Bồng Lai, Cách Bi
- **Phường Đào Viên**: Phù Lương, Ngọc Xá, Đào Viên
- **Phường Nhân Hòa**: Nhân Hòa, Đại Xuân, Việt Thống
- **Phường Phương Liễu**: Phượng Mao, Phương Liễu
- **Phường Quế Võ**: Việt Hùng, Phố Mới, Bằng An
- **Xã Chi Lăng**: Chi Lăng, Yên Giả; Tân Chi (Huyện Tiên Du)
- **Xã Phù Lãng**: Phù Lãng, Châu Phong, Đức Long

#### Thị xã Thuận Thành

- **Phường Mão Điền**: An Bình, Mão Điền, Hoài Thượng
- **Phường Ninh Xá**: Ninh Xá
- **Phường Song Liễu**: Hà Mãn, Ngũ Thái
- **Phường Trạm Lộ**: Nghĩa Đạo

### Bắc Giang cũ

#### Huyện Hiệp Hòa

- **Xã Hiệp Hòa**: Đông Lỗ, Thắng, Lương Phong, Danh Thắng
- **Xã Hoàng Vân**: Hoàng Vân, Ngọc Sơn, Đồng Tiến, Toàn Thắng
- **Xã Hợp Thịnh**: Hợp Thịnh, Thường Thắng, Mai Trung, Hùng Thái, Sơn Thịnh
- **Xã Xuân Cẩm**: Hương Lâm, Châu Minh, Bắc Lý, Xuân Cẩm

#### Huyện Lạng Giang

- **Xã Kép**: Kép
- **Xã Tiên Lục**: An Hà, Đào Mỹ, Nghĩa Hưng, Nghĩa Hòa

#### Huyện Lục Nam

- **Xã Bắc Lũng**: Bắc Lũng, Khám Lạng, Lan Mẫu
- **Xã Bảo Đài**: Tam Dị, Bảo Đài, Bảo Sơn, Thanh Lâm
- **Xã Cẩm Lý**: Đan Hội, Lục Sơn
- **Xã Đông Phú**: Đông Hưng, Đông Phú
- **Xã Lục Nam**: Chu Điện, Tiên Nha, Trường Giang
- **Xã Nghĩa Phương**: Nghĩa Phương, Yên Sơn, Huyền Sơn
- **Xã Trường Sơn**: Vô Tranh

#### Huyện Lục Ngạn

- **Xã Biển Động**: Biển Động
- **Xã Biên Sơn**: Phong Vân, Biên Sơn; Thanh Hải (Thị xã Chũ)
- **Xã Lục Ngạn**: Tân Hoa, Giáp Sơn, Đồng Cốc, Tân Quang, Phì Điền
- **Xã Tân Sơn**: Tân Sơn

#### Huyện Sơn Động

- **Xã Dương Hưu**: Long Sơn, Dương Hưu
- **Xã Đại Sơn**: Giáo Liêm, Đại Sơn
- **Xã Sơn Động**: Vĩnh An, An Châu
- **Xã Tây Yên Tử**: Tây Yên Tử, Thanh Luận
- **Xã Tuấn Đạo**: Tuấn Đạo

#### Huyện Tân Yên

- **Phường Đa Mai**: Quế Nham; Tân Mỹ (Thành phố Bắc Giang) _(chỉ có ranh thửa và diện tích)_
- **Xã Ngọc Thiện**: Việt Ngọc, Ngọc Châu, Ngọc Thiện
- **Xã Nhã Nam**: Liên Sơn, Nhã Nam, An Dương
- **Xã Phúc Hòa**: Phúc Hòa, Hợp Đức _(chỉ có ranh thửa và diện tích)_
- **Xã Quang Trung**: Lam Sơn, Quang Trung
- **Xã Tân Yên**: Cao Xá, Việt Lập, Ngọc Lý, Cao Thượng

#### Huyện Yên Thế

- **Xã Bố Hạ**: Đông Sơn, Hương Vĩ
- **Xã Đồng Kỳ**: Đồng Vương, Đồng Hưu, Đồng Kỳ, Hương Vĩ
- **Xã Tam Tiến**: Tam Tiến, Tiến Thắng, An Thượng
- **Xã Xuân Lương**: Xuân Lương, Canh Nậu, Đồng Tiến
- **Xã Yên Thế**: Tân Sỏi, Tân Hiệp, Đồng Lạc, Phồn Xương, Đồng Tâm

#### Thành phố Bắc Giang

- **Phường Bắc Giang**: Thọ Xương, Xương Giang, Hoàng Văn Thụ
- **Phường Tân An**: Tân An
- **Phường Tân Tiến**: Tân Tiến, Hương Gián
- **Phường Tiền Phong**: Đồng Sơn, Song Khê, Nội Hoàng

#### Thị xã Chũ

- **Phường Chũ**: Thanh Hải, Trù Hựu, Hồng Giang, Chũ
- **Phường Phượng Sơn**: Quý Sơn, Phượng Sơn, Mỹ An
- **Xã Kiên Lao**: Kiên Lao, Kiên Thành
- **Xã Nam Dương**: Nam Dương; Tân Mộc (Huyện Lục Ngạn)

#### Thị Xã Việt Yên

- **Phường Nếnh**: Tăng Tiến, Vân Trung, Quang Châu, Quảng Minh
- **Phường Tự Lạn**: Thượng Lan, Hương Mai, Việt Tiến, Tự Lạn
- **Phường Vân Hà**: Tiên Sơn, Trung Sơn, Ninh Sơn, Vân Hà, Quảng Minh
- **Phường Việt Yên**: Nghĩa Trung, Minh Đức, Hồng Thái

**Chưa có dữ liệu:** Phường Cảnh Thụy, Phường Thuận Thành, Phường Trí Quả, Phường Yên Dũng, Xã An Lạc, Xã Đại Lai, Xã Đèo Gia, Xã Đồng Việt, Xã Gia Bình, Xã Lâm Thao, Xã Lạng Giang, Xã Lục Sơn, Xã Lương Tài, Xã Mỹ Thái, Xã Sa Lý, Xã Sơn Hải, Xã Tân Dĩnh, Xã Trung Chính, Xã Trung Kênh, Xã Vân Sơn, Xã Yên Định.
