# Role
คุณคือ Creative WebGL Developer และ Senior UX/UI Designer ที่เชี่ยวชาญการสร้าง Immersive 3D Landing Page เน้นความ "ว้าว" ขั้นสุดแต่ยังคงความสะอาดตา (Clean & Minimalist) และสื่อถึงความน่าเชื่อถือระดับองค์กร

# Context & Objective
- โปรเจกต์: `nicecenter.co.th` (หจก. ไนซ์ เซ็นเตอร์ ออยล์) ตัวแทนจำหน่ายน้ำมันเครื่องและอะไหล่ทางการกว่า 20 ปี
- เป้าหมาย: สร้าง Trust ให้คู่ค้า B2B/B2C ผ่านดีไซน์ที่ทันสมัย มี 3D Interaction ที่เกี่ยวกับธุรกิจยานยนต์และน้ำมันเครื่อง
- สไตล์: Base สีสว่างสะอาดตา (White/Cream), Glassmorphism, 3D Interactive, Smooth Scrolling

# Brand CI & Colors (Strict Rules)
1. **Nice Center Oil (Primary):**
   - Main: `#ed5b2d` (Orange - ใช้กับจุดเด่น/CTA/3D Highlights)
   - Base/Background: `#f6f6e9` (Cream) สลับกับ `#ffffff` เพื่อความสะอาดตา
   - Text/Dark Elements: `#291b25` (Dark Accent)
2. **Partners (Castrol / Denso / Niterra):**
   - Castrol Green: `#099247` | Red: `#ee0122`
   - High-performance Accent (Audi F1 Vibe): `#eb4526`, `#dfe1e2`, `#000000`

# Immersive 3D Structure & Content

## 1. Hero Section: The Fluid Dynamics (3D)
- **Visual:** ใช้ Three.js สร้าง 3D Fluid Simulation (จำลองความลื่นไหลของน้ำมันเครื่องสีอำพัน/ทอง) เคลื่อนไหวตอบสนองตามเมาส์ (Mouse-move interaction) วางบนพื้นหลังสีขาว/ครีมสว่าง
- **Copy:** - Headline: ตัวแทนจำหน่ายน้ำมันเครื่องและอะไหล่ยานยนต์อย่างเป็นทางการ
  - Sub-headline: ประสบการณ์กว่า 20 ปี มุ่งมั่นส่งมอบสินค้าแท้ 100%
- **Elements:** โลโก้แบรนด์พันธมิตร (Castrol, Denso, NGK, Mitsuboshi) ลอยอยู่แบบ Glassy effect
- **CTA:** ปุ่มกดแบบ 3D Hover Effect "ติดต่อฝ่ายขาย (Line OA)" ใช้สี `#ed5b2d`

## 2. Coverage Area: The Interactive Map
- **Visual:** นำเสนอพื้นที่บริการ 6 จังหวัดภาคกลาง (สุพรรณบุรี, สิงห์บุรี, อ่างทอง, อุทัยธานี, ชัยนาท, นครสวรรค์) ด้วยโมเดล/แผนที่ 3D หรือ Parallax Map เมื่อเลื่อนเมาส์ผ่านแต่ละพื้นที่จะมีแสง Highlight สื่อถึงการดูแลโดยทีมงาน DSR
- **Copy:** ครอบคลุมพื้นที่ 6 จังหวัด พร้อมทีมงาน DSR ดูแลใกล้ชิด

## 3. Product Visualization: Orbit & Exploded View
- **Visual:** การ์ดสินค้าแบบ Glassmorphism นำเสนอ 4 กลุ่มหลัก:
  1. Castrol (น้ำมันเครื่อง)
  2. Denso (กรองน้ำมัน/หัวเทียน)
  3. Niterra/NGK (หัวเทียน)
  4. Mitsuboshi (สายพาน)
- **3D Interaction:** เมื่อ Hover ที่การ์ด ให้มีเอฟเฟกต์หมุนดูชิ้นส่วนได้ (Orbit) หรือแอนิเมชันชิ้นส่วนประกอบกัน (Mockup ด้วย CSS 3D Transforms หรือ Three.js เบื้องต้น)

## 4. Trust & Infrastructure (Scroll Animations)
- **Visual:** เล่าเรื่องผ่าน GSAP ScrollTrigger 
- **Copy & Facts:** - ดำเนินธุรกิจมานานกว่า 20 ปี 
  - คลังสินค้าใหม่และศูนย์ปฏิบัติการที่ อู่ทอง สุพรรณบุรี (รองรับสต็อกสินค้าจำนวนมาก)
  - ขับเคลื่อนด้วยทีมงานคุณภาพ: แอดมิน, DSR และทีมจัดส่งของตัวเอง
- **Animation:** ตัวเลขสถิติ (20+ ปี, 6 จังหวัด) วิ่งนับขึ้น (Count up) เมื่อเลื่อนมาถึง

## 5. Footer (Dark Contrast)
- พื้นหลังเปลี่ยนเป็นสี `#291b25` เพื่อปิดท้ายอย่างหนักแน่น
- **ข้อมูล:** - หจก. ไนซ์ เซ็นเตอร์ ออยล์ (212 ม.5 ซ.สำนักเกษตร ต.อู่ทอง อ.อู่ทอง จ.สุพรรณบุรี)
  - เปิดทำการ: จันทร์-เสาร์ 08:30-17:00
  - โทร: 063-202-9333 | Line: @356csnbc

# Technical Implementation
1. เขียนเป็น Single HTML File
2. ใช้ **Tailwind CSS** สำหรับ Layout และ Styling
3. เรียกใช้ **Three.js** (ผ่าน CDN) สำหรับ 3D Fluid / Particle พื้นหลัง
4. เรียกใช้ **GSAP + ScrollTrigger** (ผ่าน CDN) สำหรับแอนิเมชันตอนเลื่อนหน้าจอ
5. โค้ดต้อง Clean, Responsive 100% และสามารถ Preview ผ่าน Claude Artifacts ได้ทันที (ระวังเรื่อง CORS ของโมเดล 3D ให้ใช้ Procedural Generation เช่น Particle System หรือ Fluid Shader แทนการโหลดไฟล์ .gltf ภายนอกเพื่อให้รันในพรีวิวได้)