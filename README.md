# Multibots are evolving | Çoxlu Bot'u Birdən Yerləşdir 🧑🏻‍💻

_Daha az resurslu Telegram Botlarını pulsuz yerləşdirməli olduğunuz problemlə qarşılaşdınızmı və siz yalnız bir hesab üçün bir bot yerləşdirə bilərsiniz, lakin bütün botları bir instansiyada yerləşdirmək istəyirdiniz və bunla qarşılaşdınız... 😁_

 _Eyni instansiyada birdən çox bot işlədə bilərsiniz, hələlik o, yalnız saf ⚕ piton botları üçün işləyir (hələ docker dəstəyi yoxdur), lakin siz bunu Docker dəstəyini təmin edən xidmətlərdə yerləşdirməlisiniz._



## Necə istifadə etməli ⁉️

1. *Reponu Klonlayın*
2. *CONFIG.json-u istədiyiniz kimi ( Bot'lara əsasan ) redaktə edin*
3. *Repounu Hostingə Yerləşdirin*
4. *Və Rahatlıqla İstifadə edin*



## Xüsusiyyətlər 🔘


 ⎋  **Bot Sayı:** siz sadəcə daha çox obyekt əlavə etməklə bunu istənilən sayda botlara genişləndirə bilərsiniz (baxın [məsələn](#Nümunə) aşağıda), baxmayaraq ki, 500 mb yaddaş üçün 5 bot'u keçməməyi tövsiyə edirəm.
 ⎋  **Configlər:**, hətta eyni adlı müxtəlif botlar üçün müxtəlif config dəyərləri təyin edə bilərsiniz.
 ⎋  **Nəzarət:** siz həmçinin həmin bot üçün icranın başladığı yerdən skript faylını təyin edə bilərsiniz.
 ⎋  **Şəxsi Repo:** siz həmçinin tokenlərin köməyi ilə şəxsi depoları klonlaya bilərsiniz.  (aşağıda [məsələn](#Nümunə) baxın)
 ⎋  **Web sayt yerləşdirmək:** tövsiyə saytlar - [render](https://render.com/), [scalingo](https:  //scalingo.com/) və s.

---

## Nümunə 

```
{   
    "bot1": {
        "source": "https://github.com/rzayevaga/public-bot",
        "env": {
            "BOT_TOKEN": "bot_token@t.me/botfather"
            "API_ID": "api_id@my-telegram-org/apps"
            "API_HASH": "api_hash@my-telegram-org/apps"
        },
        "run": "bot1.py"
    },
    "bot2": {
        "source": "https://github.com/rzayevaga/public-bot.git",
        "env": {
            "BOT_TOKEN": "bot_token@t.me/botfather"
            "API_ID": "api_id@my-telegram-org/apps"
            "API_HASH": "api_hash@my-telegram-org/apps"
        },
        "run": "bot3.py"
    },
    "bot3": {
        "source": "https://github.com:ghp_token@github.com/rzayevaga/private-bot.git",
        "env": {
            "BOT_TOKEN": "bot_token@t.me/botfather"
            "API_ID": "api_id@my-telegram-org/apps"
            "API_HASH": "api_hash@my-telegram-org/apps"
        },
        "run": "bot3.py"
    }
}
```