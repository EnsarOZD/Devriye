# Akyıldız Devriye Takip Sistemi 🛡️
Akyıldız Lojistik ve Tesis Yönetimi için geliştirilmiş, Vue 3 ve Firebase tabanlı modern bir devriye takip uygulamasıdır. Güvenlik personelinin QR kod okutarak noktaları denetlemesini sağlar ve yöneticilere gerçek zamanlı raporlama sunar.
## 🚀 Temel Özellikler
- **📱 PWA Desteği**: Uygulama olarak telefona kurulabilir ve bildirimler alınabilir.
- **🔍 QR Kontrol Noktaları**: Her nokta için dinamik QR kod oluşturma ve yazdırma (A4 Poster/Etiket formatları).
- **📊 Gelişmiş Raporlama**:
  - Günlük devriye tamamlama oranları.
  - Eksik veya geciken noktaların anlık takibi.
  - PDF ve Excel formatında dışa aktarma.
- **🚨 Acil Durum (SOS)**: Personel için saniyeler içinde merkeze uyarı gönderen SOS butonu.
- **🔔 Anlık Bildirimler**: Kaçırılan devriyeler veya kritik olaylar için yöneticiye anlık push bildirimleri.
- **🕒 Planlama (Schedules)**: Belirli saat aralıkları için devriye görevleri tanımlama.
## 🛠️ Teknoloji Yığını
- **Frontend**: Vue 3 (Composition API), Vite, Tailwind CSS.
- **State Management**: Pinia.
- **Backend**: Firebase (Firestore, Auth, Realtime Database, Cloud Messaging).
- **Test**: Vitest, Vue Test Utils (Kapsamlı mock altyapısı ile).
- **Raporlama**: jsPDF, XLSX.
## ⚙️ Kurulum ve Çalıştırma
### 1. Projeyi Klonlayın
```bash
git clone https://github.com/kullanici/akyildiz-devriye.git
cd akyildiz-devriye
```
### 2. Bağımlılıkları Kurun
```bash
npm install
```
### 3. Çevre Değişkenlerini Ayarlayın
`.env` dosyası oluşturun ve Firebase anahtarlarınızı ekleyin:
```env
VITE_FIREBASE_API_KEY=your_key
VITE_FIREBASE_AUTH_DOMAIN=your_domain
...
```
### 4. Geliştirme Ortamını Başlatın
```bash
npm run dev
```
### 5. Testleri Çalıştırın
```bash
npm test          # Standart testler
npm run test:ui   # Görsel test arayüzü
```
## 📂 Proje Yapısı
- `src/views`: Sayfa bileşenleri (AdminPanel, PatrolView vb.).
- `src/components`: Tekrar kullanılabilir UI bileşenleri (QrScanner, AdminLayout).
- `src/services`: Firebase ve bildirim servisleri.
- `src/utils`: Tarih ve zaman yardımcıları.
- `functions`: Firebase Cloud Functions (Zamanlanmış görevler ve bildirimler).
## 🔒 Güvenlik
Proje, Firebase Security Rules ile korunmaktadır. Kritik işlemler yalnızca sistemde tanımlı yönetici e-posta adresleri (`ADMIN_EMAILS`) tarafından gerçekleştirilebilir.
---
© 2026 Akyıldız Lojistik - Tüm Hakları Saklıdır.
