# 💳 Kredi & Banka Kartı Format Doğrulama Aracı

![Lisans: MIT](https://img.shields.io/badge/Lisans-MIT-blue.svg)
![PR'lar Açık](https://img.shields.io/badge/PR'lar-kabul_edilir-brightgreen.svg)
![Vanilla JS](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)

Dünyadaki tüm standart ödeme kartlarının (Visa, Mastercard, TROY, Amex vb.) kart numarası, son kullanma tarihi (SKT) ve CVC/CVV güvenlik kodlarını format ve algoritma seviyesinde doğrulayan açık kaynaklı web uygulaması.

---

## 📌 Bu Araç Ne İşe Yarar?

Girdiğiniz kart bilgilerinin biçimsel ve matematiksel olarak geçerli olup olmadığını anında doğrular:

1. **Kart Numarası (Luhn Algoritması):** Dünyadaki tüm banka ve kredi kartlarının uymak zorunda olduğu küresel **Luhn Algoritması (Mod 10)** ile kart numarasının matematiksel doğruluğunu kontrol eder.
2. **Son Kullanma Tarihi (SKT):** Ay/Yıl formatını ve kartın süresinin dolup dolmadığını (geçmiş tarihli olup olmadığını) kontrol eder.
3. **CVC / CVV Kodu:** Kart tipine göre (Visa/Mastercard için 3 haneli, Amex için 4 haneli) güvenlik kodunun formatını doğrular.
4. **Anlık Kart Ağı Tespiti:** Girilen ilk hanelerden (BIN/IIN) kartın Visa, Mastercard, TROY veya Amex olduğunu algılar.

---

## ✨ Öne Çıkan Özellikler

- **Küresel Standart:** ISO/IEC 7812 standardına uygun tüm uluslararası kart numaralarıyla çalışır.
- **Canlı Kart Markası Algılama:** 
  - 🔵 **Visa** (4 ile başlayanlar)
  - 🔴 **Mastercard** (51-55 veya 22-27 aralığı)
  - 🔴 **TROY** (9792 ile başlayanlar)
  - 🟢 **American Express** (34 veya 37 ile başlayanlar)
- **Akıllı Maskeleme & Biçimlendirme:** Kart yazılırken `XXXX XXXX XXXX XXXX` şeklinde otomatik boşluklandırılır, SKT alanına otomatik `/` eklenir.
- **%100 İstemci Taraflı (Client-Side) Güvenlik:** Kod tamamen tarayıcınızda çalışır. Verileriniz hiçbir sunucuya gönderilmez, kaydedilmez ve üçüncü taraflarla paylaşılmaz.
