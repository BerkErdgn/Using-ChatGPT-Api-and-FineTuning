# Using-ChatGPT-Api-and-FineTuning

## Genel Bakış

Bu script, OpenAI API kullanarak ChatGPT modelini fine-tune etme sürecini detaylı bir şekilde sağlar. Özel bir veri kümesi oluşturma, modeli fine-tune etme ve fine-tune edilmiş modelle istek yapma süreçlerini kapsar.

## Önkoşullar

Script çalıştırmadan önce gerekli Python kütüphanelerinin yüklü olduğundan emin olun:

```bash
pip install openai tiktoken json requests os time
```

Ayrıca, OpenAI API anahtarınızın olduğundan emin olun ve bu anahtarı `OPENAI_API_KEY` değişkenine ekleyin.

## Kullanım

1. **ChatGPT İstekleri:**
   - API anahtarınızı `OPENAI_API_KEY` değişkenine ekleyin.
   - Scripti çalıştırarak ChatGPT'ye belirli bir görev için istekte bulunun, örneğin bir şiir oluşturun veya bir programlama kavramını açıklayın.

2. **Fine-tuning:**
   - `json_script` ve `json_script_validation` değişkenlerini, eğitim ve doğrulama verilerinizi istediğiniz formatta düzenleyin.
   - Scripti çalıştırarak eğitim ve doğrulama veri setlerini oluşturun.
   - Veri seti istatistiklerini, token dağılımını kontrol edin ve token maliyetini hesaplayın.
   - Eğitim ve doğrulama veri setlerini OpenAI'e Dosyalar API'si kullanarak yükleyin.

3. **Modeli Fine-tune Etme:**
   - Eğitim ve doğrulama veri setleri için dosya kimliklerini alın.
   - Fine-tune işlemi oluşturarak ChatGPT modelini fine-tune edin.
   - İş durumunu izleyin ve ilgili bilgileri alın.

4. **Fine-tune Edilmiş Model ile Çıkarımlar:**
   - OpenAI API'ye istek yaparak belirli görevler için fine-tune edilmiş modeli kullanın.
   - Kullanıcı sorguları ve sistem mesajları için tamamlamayı kontrol edin.

5. **Temizlik:**
   - Artık gerekli olmadığında fine-tune edilmiş modeli silerek gereksiz maliyetlerden kaçının.

**Not:** Fine-tuning işlemleri ve model oluşturma süreçleri oldukça uzun sürebilir. Sabırlı olun ve gerektiğinde ilerlemeyi izleyin.

## Uyarı

OpenAI'nin fine-tuning kullanım politikalarını anladığınızdan ve uyduğunuzdan emin olun. Bu örnek kod, ChatGPT'nin yeteneklerini hatırlamak ve daha sonraki benzer görevlerde kullanılması için yazılmıştır. Alınan eğitimi tekrarlamak ve hızlı bir şekilde benzer görevleri gerçekleştirmek amacıyla kullanılması için yazılmıştır
