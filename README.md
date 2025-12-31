🖋️ Piórniczek - HomeLab Dashboard 🚀
Witaj w Piórniczku! To minimalistyczny, szybki i nowoczesny dashboard stworzony specjalnie do zarządzania Twoim domowym ekosystemem aplikacji webowych.
Zapomnij o wpisywaniu portów (np. :8001) i adresów IP. Teraz wszystko masz w zasięgu jednego kliknięcia pod domeną piorniczek.manowski.pl.
🌟 Główne Funkcje
 * 🎨 Modern UI – Czysty design oparty na Tailwind CSS z ciemnym motywem (Dark Mode).
 * 📱 Fully Responsive – Idealnie wygląda na smartfonie, tablecie i desktopie.
 * ⚡ Ultra Lekki – Zero ciężkich frameworków, błyskawiczne ładowanie.
 * 🔗 Reverse Proxy Friendly – Zaprojektowany do pracy z NGINX, Gunicorn i Flaskiem.
 * 🧩 Łatwa Konfiguracja – Dodanie nowej aplikacji to tylko edycja jednej tablicy w kodzie.
🏗️ Architektura Systemu
Dashboard stanowi centralny punkt (Entry Point) Twojego serwera:
 * Użytkownik wchodzi na piorniczek.manowski.pl.
 * NGINX (Reverse Proxy) serwuje ten dashboard.
 * Wybranie aplikacji przekierowuje na odpowiednią subdomenę (np. app1.piorniczek.manowski.pl).
 * NGINX przekierowuje ruch wewnątrz serwera do odpowiedniego portu, na którym działa Gunicorn z Twoim Flaskiem.
🛠️ Jak dodać nową aplikację?
Wystarczy edytować plik index.html (lub odpowiedni widok we Flasku) i zaktualizować listę applications:
{
    name: "Twoja Nowa Apka",
    description: "Krótki opis tego, co robi ta aplikacja.",
    url: "[https://nowa-apka.piorniczek.manowski.pl](https://nowa-apka.piorniczek.manowski.pl)",
    icon: "🔥"
}

📦 Szybki Start (Deployment)
Aby uruchomić dashboard na swoim serwerze:
 * Sklonuj repozytorium:
   git clone [https://github.com/TwojUser/homelab-dashboard.git](https://github.com/TwojUser/homelab-dashboard.git)

 * Skonfiguruj NGINX:
   Dodaj nowy blok server dla swojej domeny głównej.
 * Zrestartuj usługi:
   sudo systemctl restart nginx

🛰️ Technologie
 *  *  *  *  * 👤 Autor
Manowski – Pasjonat HomeLabu i czystego kodu.
⭐ Jeśli ten projekt Ci się podoba, zostaw gwiazdkę!
