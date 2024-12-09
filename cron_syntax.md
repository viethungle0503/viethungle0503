# Cú pháp Cron:

## Generator
Please visit https://crontab.guru to get more insights about cron syntax

## Giải thích
Cú pháp Cron bao gồm 5 trường, mỗi trường đại diện cho một đơn vị thời gian khác nhau:

- Phút: 0-59
- Giờ: 0-23
- Ngày: 1-31
- Tháng: 1-12
- Ngày trong tuần: 0-7 (0 hoặc 7 là Chủ nhật)
- Phân tích đoạn code: `schedule: [{cron: "0 * * * *"}]`. `0 * * * *`: Nghĩa là cứ mỗi phút thứ 0 của mọi giờ, mọi ngày, mọi tháng, mọi ngày trong tuần, workflow sẽ chạy.

## Ví dụ
### Chạy vào ngày cuối cùng của mỗi tháng:
`schedule: [{cron: "0 0 L * *"}]` với (L đại diện cho "last")
### Chạy vào ngày thứ 3 của mỗi tháng:

`schedule: [{cron: "0 0 3 * *"}]`
### Chạy vào ngày thứ 7 đầu tiên của mỗi tháng:

`schedule: [{cron: "0 0 1W * *"}]` với 1W đại diện cho "weekdays" và sẽ chọn ngày thứ 7 đầu tiên trong tháng