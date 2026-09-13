🤖 AI-Powered Smart Web Scraper
Playwright ve Google GenAI SDK (Gemini 3.6 Flash) kullanılarak geliştirilmiş, e-ticaret ve dinamik web sayfalarından yapılandırılmış veri (JSON) ayıklayan açık kaynaklı akıllı web kazıma aracı.

🚀 Özellikler
Dinamik Sayfa Desteği: Playwright ile JavaScript ağırlıklı sayfaları otomatik yükler ve simüle eder.

Esnek AI Analizi: Karmaşık HTML ve DOM bağımlı CSS seçicileri yerine gemini-3.6-flash modeli ile bağlamsal veri ayıklama yapar.

Tip Güvenliği ve Şema Doğrulama: Pydantic (UrunVerisi) ve response_schema kullanarak sıfır hata ile JSON çıktısı üretir.

Hata Yönetimi ve Otomatik Yeniden Deneme (Backoff): 429 (Rate Limit) ve 503 (Server Unavailable) durumlarında kademeli bekleme mekanizması barındırır.

Temiz ve Formatlı Çıktı: Çıkarılan verileri otomatik olarak indent=2 biçiminde output.json dosyasına kaydeder.

🛠️ Kurulum
Repoyu klonlayın:
git clone https://github.com/KULLANICI_ADINIZ/ai-web-scraper.git
cd ai-web-scraper

Sanal ortam (virtual environment) oluşturun ve aktifleştirin:
python -m venv venv

Windows (PowerShell):
.\venv\Scripts\activate

Windows (CMD):
.\venv\Scripts\activate.bat

macOS/Linux:
source venv/bin/activate

Gerekli bağımlılıkları yükleyin:
pip install -r requirements.txt
playwright install chromium

Çevre değişkenlerini (.env) ayarlayın:
Proje ana dizininde .env dosyası oluşturun ve API anahtarınızı ekleyin:
GEMINI_API_KEY=your_gemini_api_key_here

💻 Kullanım
Scraper'ı başlatmak için:
python scraper.py

Komut satırında istenen hedef URL'yi yapıştırın. Çıktılar otomatik olarak output.json dosyasına yazılacaktır.

📊 Örnek Çıktı
[
{
"urun_adi": "A Light in the Attic",
"fiyat": "£51.77",
"stokta_mi": true
}
]
