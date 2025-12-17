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
```

## 🚗 Kontrol Mantığı

Robot önce hedefe doğru hizalanır
Yeterince hizalandığında:
İleri gider
Küçük açısal sapmalar için düzeltme yapar.

Hedefe ulaşıldığında:
Yeni rastgele hedef oluşturulur
 
## Çalıştırma
pip install pybullet
python robot_env.py

Simülasyon GUI modunda açılır ve robot hedeflere doğru otonom şekilde hareket eder.

##  Kullanım Amacı
Mobil robot navigasyonu
Reinforcement Learning ortamı geliştirme
PyBullet ve diferansiyel sürüş deneyleri
Akademik / eğitim amaçlı simülasyon

## Sonraki Adımlar

Episode & reset mekanizması
Engel (obstacle) eklenmesi
Ödül fonksiyonu tasarımı
Q-learning / PPO ile eğitim

## Lisans

Bu proje eğitim ve araştırma amaçlıdır.
