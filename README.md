# TelephoneSpeaks
TGN/TPS Global 
Project overview & setup instructions

```python
from PIL import Image, ImageDraw, ImageFont

*"Devices can be anywhere, but communication is limited—when technology reaches people's hearts around the world at their fingertips."*

สร้างภาพเปล่าขนาด 512x512 พื้นหลังดำ
img = Image.new('RGB', (512, 512), color='black')

draw = ImageDraw.Draw(img)
font = ImageFont.load_default()

วาดวงแหวนสีรุ้ง
for i in range(50):
    bbox = [50+i*3, 50+i*3, 462-i*3, 462-i*3]
    color = (255 - i*5, i*5, 150)
    draw.ellipse(bbox, outline=color, width=5)

เขียนข้อความตรงกลาง
draw.text((180, 240), "Meta AI", font=font, fill=(255,255,255))


🔁 *TPspeak (Speech I/O) Functionality:*

1. *STT (Speech-to-Text)*
Converts user speech → to text
(Sent to GPT via Lots Server)

2. *Lots Server / GPT: TPspeak*
Central Processing:
- Receive text from STT
- Analyze with GPT
- Generate response

3. *TTS (Text-to-Speech)*
Convert text from GPT → back to speech

To respond to the user

4. *Text ⇄ Speech Integration*
Supports seamless switching between speech and text

---

🧠 Benefits:
- Ideal for WhatsApp, Line, Telegram, or IoT devices that support voice
- Supports multiple languages
บันทึกภาพ
img.save("meta_ai_ring.png")
```

---


```markdown
![Meta AI Ring](meta_ai_ring.png)
```

---
