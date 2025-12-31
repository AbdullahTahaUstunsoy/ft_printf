# ft_printf - Because Putchar is Not Enough

ft_printf, C dilindeki standart `printf` fonksiyonunu yeniden oluşturduğumuz bir **42 School** projesidir. Temel amacı, değişken sayıda argüman alan fonksiyonların (variadic functions) çalışma mantığını kavramak ve verileri belirli formatlara göre ekrana yazdırmaktır.

---

## Özellikler

- **Geniş Format Desteği:** Standart printf fonksiyonunun temel dönüştürücülerini destekler:
  - `%c` (karakter), `%s` (dizgi), `%p` (işaretçi adresi).
  - `%d` / `%i` (tam sayı), `%u` (işaretsiz tam sayı).
  - `%x` / `%X` (onaltılık taban - küçük/büyük harf), `%%` (yüzde işareti).
- **Hassasiyet ve Doğruluk:** Standart kütüphane ile aynı dönüş değerlerini (yazdırılan karakter sayısı) ve çıktıları sağlar.
- **Modüler Yapı:** Kolayca genişletilebilir ve farklı projelere dahil edilebilir temiz bir kod yapısına sahiptir.

---

## Teknik Kazanımlar

Bu proje süresince C programlamanın ileri seviye konularında şu yetkinlikleri kazandım:
- **Variadic Functions:** `stdarg.h` kütüphanesini kullanarak `va_list`, `va_start`, `va_arg` ve `va_end` makroları ile belirsiz sayıda argüman yönetimi.
- **Veri Dönüştürme Algoritmaları:** Sayısal verilerin farklı tabanlarda (onluk, onaltılık) temsil edilmesi ve karakter dizisi olarak işlenmesi.
- **Format Ayrıştırma (Parsing):** Kullanıcıdan gelen format dizgisini analiz ederek doğru dönüştürücüyü tetikleyen bir yapı kurma.
- **Kod Entegrasyonu:** Fonksiyonu bir kütüphane (`libft.a`) içine dahil ederek diğer projelerde tekrar kullanılabilir hale getirme.

---

## Kurulum ve Kullanım

1. **Depoyu klonlayın:**
   ```bash
   git clone [https://github.com/AbdullahTahaUstunsoy/ft_printf.git](https://github.com/AbdullahTahaUstunsoy/ft_printf.git)
   cd ft_printf
2. Kütüphaneyi derleyin: Terminalde make komutunu çalıştırarak kaynak dosyalarını derleyin; bu işlem sonucunda libftprintf.a adında bir statik kütüphane dosyası oluşturulacaktır.
3. Projenizde kullanın: Kendi projelerinizde ft_printf fonksiyonunu kullanmak için ft_printf.h başlık dosyasını dahil etmeli ve derleme aşamasında oluşturduğunuz .a dosyasını (örneğin gcc main.c libftprintf.a) bağlamalısınız.
