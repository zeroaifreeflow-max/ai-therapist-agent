# สรุปการทำงานของ Aura 3.0 (Project Overview & Logic)

**Aura 3.0** คือระบบตัวแทนอัจฉริยะ (AI Agent) สำหรับการดูแลสุขภาพจิตแบบครบวงจร ที่ผสานพลังของ AI ขั้นสูงเข้ากับความปลอดภัยของเทคโนโลยี Blockchain บนเครือข่าย Sonic

---

## 🧠 1. Core AI Therapy Logic (ระบบวิเคราะห์อารมณ์)

Aura ทำหน้าที่เป็นนักบำบัดส่วนตัวที่ใช้เฟรมเวิร์ก **Zerepy** และโมเดล **Gemini 1.5 Flash / GPT-4** ในการประมวลผล:

- **Emotional Intelligence:** วิเคราะห์สถานะทางอารมณ์ (Emotional State) จากข้อความแชทของผู้ใช้ในทุก Turn
- **Context-Aware Response:** ปรับเปลี่ยนบุคลิกภาพ (Personality) และแนวทางการพูดคุย (Therapy Approach) ให้เหมาะสมกับสภาวะจิตใจ ณ ขณะนั้น
- **Crisis Detection:** มีระบบตรวจจับสัญญาณความเครียดและคำสำคัญที่เป็นอันตราย (Stress Signal Pattern) เพื่อเข้าสู่โปรโตคอลช่วยเหลือฉุกเฉินทันที

---

## 🤖 2. Deep Dive: Zerepy AI Framework (สมองของ Aura)

Aura 3.0 ขับเคลื่อนด้วยเฟรมเวิร์ก **Zerepy** ซึ่งเป็นระบบ Autonomous Agent ที่มีความซับซ้อน:

- **Multi-Agent Coordination:** Zerepy ไม่ได้ทำงานเพียงตัวเดียว แต่มีโครงสร้างที่สามารถประสานงานระหว่างเอเจนท์ที่มีความเชี่ยวชาญเฉพาะด้าน (Specialties) เพื่อให้การดูแลครอบคลุมทั้งด้านจิตวิทยาและข้อมูลสุขภาพทั่วไป

- **Dynamic Personality Adaptation:** ปรับเปลี่ยน "Personality" และ "Therapy Approach" (เช่น CBT, Dialectical Behavior Therapy) ตามข้อมูลโปรไฟล์และอารมณ์ของผู้ใช้แบบ Real-time

- **Configurable Agent Architecture:**
  
  ```typescript
  class TherapyAgentConfig {
    name: "Aura",
    personality: "Empathetic, non-judgmental, professional",
    language_model: "gemini-1.5-flash" | "gpt-4",
    temperature: 0.7, // เพื่อความสมดุลระหว่างความสร้างสรรค์และความแม่นยำ
    specialties: ["Anxiety", "Stress Management", "Mindfulness"],
    crisis_protocol: { ... } // โปรโตคอลเมื่อตรวจพบความเสี่ยงสูง
  }
  ```

- **Continuous Learning System:** ระบบสามารถเรียนรู้จากบทสนทนาที่ผ่านมา (Session History) เพื่อให้การปรึกษาในครั้งถัดไปมีความต่อเนื่องและตรงจุดมากขึ้น (Long-term Memory)

---

## ⛓️ 3. Blockchain & Security Logic (ความปลอดภัยและความเป็นส่วนตัว)

การทำงานของ Aura ถูกผูกติดกับเครือข่าย **Sonic Blaze Testnet** เพื่อให้มั่นใจในความโปร่งใสและปลอดภัย:

- **Smart Contract Session:** บันทึกข้อมูลสรุปการบำบัด (Session Summary), หัวข้อที่คุย (Topics) และคะแนนอารมณ์ (Mood Score) ลงในบล็อกเชน
- **Data Privacy:** ใช้มาตรฐานการเข้ารหัสแบบ End-to-End และสอดคล้องกับมาตรฐาน HIPAA เพื่อป้องกันข้อมูลส่วนตัวของผู้ใช้
- **NFT Achievement:** เมื่อผู้ใช้ผ่านเป้าหมายการบำบัด ระบบจะ Mint NFT (ERC-721) เพื่อเป็นเครื่องหมายยืนยันความก้าวหน้า (Milestones)

---

## 📈 3. Monitoring & Gamification Logic (การติดตามผลและแรงจูงใจ)

Aura มีระบบ Dashboard ที่ช่วยให้ผู้ใช้เห็นพัฒนาการของตัวเอง:

- **Mood Tracking:** ระบบคำนวณคะแนนอารมณ์เฉลี่ย (Average Mood Score) และแสดงผลเป็นกราฟสถิติรายวัน/รายสัปดาห์
- **Token Rewards (Sonic Token):** ให้รางวัลผู้ใช้เป็น Sonic Token เมื่อทำกิจกรรมบำบัด เช่น การฝึกหายใจ (Breathing Exercises) หรือการดูแลสวน Zen (Zen Garden)
- **Activity Logging:** บันทึกกิจกรรมทุกอย่างทั้งในส่วนของ AI Chat และกิจกรรมคลายเครียดอื่นๆ (Activities) เพื่อนำมาประมวลผลความคืบหน้า

---

## ⛓️ 4. Technical Architecture (โครงสร้างทางเทคนิค)

- **Frontend:** Next.js (TypeScript), Tailwind CSS, Shadcn/UI
- **AI Framework:** Zerepy Integration
- **Blockchain:** Solidity Smart Contracts (Sonic Blaze Testnet)
- **API Support:** ระบบจัดการ Session การแชทและประวัติย้อนหลังผ่าน REST API ที่มีการตรวจสอบสิทธิ์ (JWT/Token)

---

## 🔄 5. Data Pipeline & Workflow (กระบวนการทำงาน)

กระบวนการรับและส่งข้อมูลของ Aura มีขั้นตอนดังนี้:

1. **Input Stage:** ผู้ใช้พิมพ์ข้อความผ่านหน้า UI (Fixed Chat หรือ Therapy Page)
2. **Frontend Proxy:** Next.js API Routes รับข้อความและส่งต่อ (Forward) ไปยัง Core Backend (Zerepy Agent) พร้อมกับ Token ตรวจสอบสิทธิ์
3. **AI Analysis (Processing):**
   - **NLU Processing:** ถอดความหมายและเจตนาของผู้ใช้
   - **Emotion & Risk Scan:** ประเมินความเสี่ยงและระดับอารมณ์ในทันที
   - **Response Generation:** สร้างคำตอบที่เหมาะสมตามหลักจิตวิทยา (CBT/Mindfulness)
4. **Metadata Enrichment:** ระบบจะแนบข้อมูล Metadata (Technique used, Goal, Analysis) กลับมาพร้อมกับคำตอบของ AI
5. **Data Synchronization:**
   - ข้อมูล Mood Score จะถูกส่งไปอัปเดตที่ Dashboard
   - เมื่อจบ Session สรุปการสนทนาจะถูกบันทึกลงฐานข้อมูลและส่งไปบันทึก (Hash/Summary) บน **Sonic Blockchain**
6. **Reward Trigger:** หากกิจกรรมนั้นตรงตามเงื่อนไข (เช่น บันทึกอารมณ์ครบ 7 วัน) ระบบจะเรียก Smart Contract เพื่อมอบ Sonic Token หรือ NFT ให้กับผู้ใช้

---

## 🌈 6. Therapeutic Features (ฟีเจอร์เพื่อการบำบัด)

- **Expandable Chat:** ระบบแชทที่เข้าถึงได้ง่ายจากทุกหน้าของแอปพลิเคชัน
- **Interactive Games:** กิจกรรมคลายเครียด เช่น การฝึกลมหายใจ, เสียงคลื่นทะเล, เดินป่าเสมือนจริง
- **Daily Check-ins:** ระบบบันทึกอารมณ์ประจำวันเพื่อวิเคราะห์แนวโน้มสุขภาพจิตในระยะยาว

---

*สรุปโดย Aura 3.0 Agent - 2026*
