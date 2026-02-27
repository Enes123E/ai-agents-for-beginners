# Enes - AI Agents For Beginners Kurs İlerleme Dosyası

## Kurs: [AI Agents For Beginners](https://github.com/microsoft/ai-agents-for-beginners)

---

## Kurulum (Tamamlandı ✅)

- [x] Repo fork'landı
- [x] GitHub Codespaces kuruldu
- [x] `az login --use-device-code` ile Azure'a giriş yapıldı
- [x] Microsoft Foundry'de hub ve proje oluşturuldu
  - Proje adı: `erasmus-ai-agent-beginners-active`
  - Resource: `erasmus-ai-agent-beginn-resource` (AI Foundry, Sweden Central)
- [x] `gpt-4o-mini` modeli deploy edildi (Global Standard, 250K TPM)
- [x] Azure AI Search kaynağı oluşturuldu
  - Kaynak adı: `erasmus-ai-agent-for-beginners`
  - Konum: North Europe
  - Fiyatlandırma: Free
- [x] `.env` dosyası oluşturuldu ve dolduruldu

### .env Dosyası İçeriği (Yarın Tekrar Oluşturulacak)
```
AZURE_AI_PROJECT_ENDPOINT="https://erasmus-ai-agent-beginn-resource.services.ai.azure.com/api/projects/erasmus-ai-agent-beginners-active"
AZURE_AI_MODEL_DEPLOYMENT_NAME="gpt-4o-mini"
AZURE_SEARCH_SERVICE_ENDPOINT="https://erasmus-ai-agent-for-beginners.search.windows.net"
AZURE_SEARCH_API_KEY="buraya_kendi_key_ini_yaz"
```

> ⚠️ Yarın Codespaces açınca şunları tekrar yapman gerekecek:
> 1. `az login --use-device-code` ile Azure girişi
> 2. `.env` dosyasını tekrar oluştur: `cp .env.example .env` → içini doldur

---

## Tamamlanan Dersler

### ✅ Ders 00 - Course Setup
- Kurulum tamamen tamamlandı.

### ✅ Ders 01 - Introduction to AI Agents
- `01-python-agent-framework.ipynb` notebook'u çalıştırıldı.
- Travel Agent oluşturuldu, tool kullanımı öğrenildi.
- Session kullanarak çok turlu konuşma yapıldı.
- Input ile interaktif konuşma kodu yazıldı:

```python
session = agent.create_session()

while True:
    user_input = input("Sen: ")
    if user_input.lower() == "çıkış":
        break
    response = await agent.run(user_input, session=session)
    print(f"Agent: {response}\n")
```

### ✅ Ders 02 - Exploring Agentic Frameworks
- `02-python-agent-framework.ipynb` notebook'u çalıştırıldı.
- Microsoft Agent Framework (MAF) ve Azure AI Agent Service farkları öğrenildi.
- Foundry portalında UI üzerinden FlightAgent benzeri bir agent oluşturma egzersizi yapıldı.
- Temperature ve Top P kavramları öğrenildi.

---

## Sıradaki Ders
**Ders 03 - Understanding Agentic Design Patterns**
- Dosya yolu: `03-agentic-design-patterns/`

---

## Öğrenilen Önemli Kavramlar

- **AI Agent**: LLM'e araçlar ve bilgi vererek gerçek dünyada aksiyon alabilen sistem.
- **Tool**: Agent'ın çağırabileceği Python fonksiyonu.
- **Session**: Agent'ın konuşma geçmişini hatırlamasını sağlar.
- **MAF (Microsoft Agent Framework)**: Hızlı agent geliştirme SDK'sı.
- **Azure AI Agent Service**: Production için enterprise platform.
- **Temperature**: Modelin yaratıcılığını kontrol eder, yüzdeleri değiştirir.
- **Top P**: Kaç seçenek arasından seçim yapılacağını kontrol eder, listeyi kırpar.
- **az login**: Azure CLI ile kimlik doğrulama, API key gerekmez.
- **Virtual Environment (.venv)**: Python paketlerini izole ortamda tutar.
