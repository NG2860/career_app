#  V-Career Korea 2035: AI-Ready Career Guidance System

**Hệ thống hướng nghiệp chuyên sâu dành cho du học sinh Việt Nam tại Hàn Quốc (Giai đoạn 2026–2035)**

---

##  Tổng quan dự án

V-Career Korea 2035 không chỉ là một bài trắc nghiệm tính cách thông thường. Đây là hệ thống **hỗ trợ ra quyết định** dựa trên dữ liệu, kết hợp giữa tâm lý học truyền thống và biến số thực tế của kỷ nguyên AI tại thị trường lao động Hàn Quốc.

### Đối tượng mục tiêu:

* **D-2 Students:** Sinh viên đang học đại học/cao học muốn chọn chuyên ngành hoặc chuyển ngành.
* **D-4 Students:** Học viên tiếng Hàn đang tìm kiếm định hướng lên đại học.
* **Fresh Graduates:** Người mới tốt nghiệp đang tìm kiếm cơ hội Visa (E-7, F-2-7) và việc làm tại Hàn.

---

## Framework tích hợp

Hệ thống sử dụng ma trận 6 lớp để phân tích dữ liệu cá nhân:

1. **MBTI:** Định vị xu hướng nạp năng lượng và giao tiếp.
2. **Holland Code (RIASEC):** Xác định sở thích nghề nghiệp cụ thể.
3. **Career Anchors:** Tìm ra "neo giá trị" (Sự ổn định, Quyền tự trị hay Thử thách).
4. **AI Adaptability:** Chỉ số sẵn sàng thích nghi với công cụ số.
5. **Visa Compatibility:** Đối chiếu nguyện vọng với thực tế chính sách cư trú tại Hàn Quốc.
6. **Future Market Demand:** Dự báo nhu cầu lao động 2026–2035.

---

## Cấu trúc Database & Khảo sát

### Section 1: Demographic & Context (Dữ liệu nền)

| Trường dữ liệu | Loại dữ liệu | Mục đích |
| --- | --- | --- |
| `Full_Name` | Text | Cá nhân hóa báo cáo |
| `Topik_Level` | Scale (1-6) | Đánh giá khả năng xâm nhập thị trường nội địa |
| `Visa_Target` | Select | Ưu tiên ổn định (F-2) hay thăng tiến (E-7) |
| `Major_Current` | Text | Phân tích tính liên kết ngành |

### Section 2: Core Assessment (Trắc nghiệm cốt lõi)

Sử dụng thang đo **Likert 1-5** cho các nhóm:

* **Logic vs Emotion:** Phân loại giữa nhóm kỹ thuật (STEM) và nhóm nhân văn.
* **Innovation vs Structure:** Phân loại giữa Startup/Sáng tạo và Tập đoàn/Hành chính.
* **AI Comfort Level:** Đo lường nỗi sợ hoặc sự hứng thú với tự động hóa.

---

##  Thuật toán phân tích (Logic Logic)

Hệ thống sẽ gán trọng số ($w$) cho các câu trả lời để tính điểm theo từng nhóm ngành:

$$Score_{AI\_Engineer} = (w_1 \cdot Logic) + (w_2 \cdot Tech\_Adapt) + (w_3 \cdot Problem\_Solving)$$

### Phân nhóm nghề nghiệp đầu ra:

1. **The Tech Architects:** (Điểm Logic + AI cao) -> *AI Engineer, Data Scientist, Cloud Ops.*
2. **The Human Connectors:** (Điểm Impact + Communication cao) -> *HR Tech, Education Consultant, Global Relations.*
3. **The Creative Strategists:** (Điểm Creativity + Digital cao) -> *UI/UX Designer, AI Content Creator, Branding.*
4. **The Backbone Admins:** (Điểm Stability + Structure cao) -> *QA, ERP Manager, Production Planning.*

---

##  Career Roadmap 2030+ (Output mẫu)

Mỗi người dùng sẽ nhận được một trang **Personalized Dashboard** với các thành phần:

### 1. Phân tích Thế mạnh (Strengths)

> "Bạn có tư duy của một **Creative Strategist**. Trong kỷ nguyên AI, bạn không bị thay thế mà là người điều khiển AI để tạo ra giá trị mới."

### 2. Gợi ý Chuyên ngành/Khóa học

* **Chuyên ngành chính:** Media & Communication / Global Business.
* **Kỹ năng bổ trợ:** Prompt Engineering, Data Visualization.

### 3. Chiến lược Visa & Sự nghiệp tại Hàn

* **Lộ trình 1:** Internship tại Startup (Pangyo) -> Visa E-7-1.
* **Lộ trình 2:** Học Master chuyên sâu về AI Social Impact -> Visa F-2-7 (Hệ thống tính điểm).

---

##  Hướng dẫn triển khai kỹ thuật (For Developers)

### Setup Frontend (React + Tailwind)

```bash
npx create-next-app v-career-2035
npm install lucide-react recharts framer-motion

```

### Data Schema (JSON)

```json
{
  "user_id": "SV12345",
  "mbti_result": "INTJ",
  "ai_readiness_score": 85,
  "top_career_matches": [
    {"job": "AI Product Manager", "match": "92%"},
    {"job": "Data Analyst", "match": "78%"}
  ]
}

---


## Tầm nhìn phát triển

* **Giai đoạn 1:** Web trắc nghiệm và xuất Report PDF.
* **Giai đoạn 2:** Kết nối Mentor (Cựu du học sinh đã đi làm tại Hàn).
* **Giai đoạn 3:** AI Coach tích hợp (Chatbot tư vấn lộ trình 24/7 dựa trên data cá nhân).

---

*© 2024 V-Career Korea Project - For the future of Vietnamese Talents.*
