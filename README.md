# 🦾 PyBullet Husky Navigation Environment

Bu proje, **PyBullet** kullanılarak geliştirilmiş, diferansiyel sürüşe sahip **Husky** robotunun
**rastgele hedeflere otonom olarak yönelmesini** sağlayan bir simülasyon ortamıdır.

---

## 🎯 Özellikler

- PyBullet tabanlı fiziksel simülasyon
- Husky diferansiyel sürüş modeli
- Rastgele oluşturulan hedef (bayrak / direk ile görselleştirme)
- Hedefe göre:
  - Mesafe (distance)
  - Yön açısı (bearing)
- Hedefe hizalanma + ileri hareket mantığı
- Gerçekçi tekerlek sürtünmesi ve motor kontrolü
- Dinamik kamera takibi

---

## 🧠 State Tanımı

Her adımda robot aşağıdaki durumu algılar:

- **Distance** → Robottan hedefe olan mesafe
- **Bearing** → Robot yönü ile hedef yönü arasındaki açı

```python
state = (distance, bearing)
