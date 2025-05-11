
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no" />
  <title>Formulir Pendaftaran Negara fiksi terbaru</title>
  <style>
    /* Reset and base */
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-image: url('https://upload.wikimedia.org/wikipedia/commons/8/80/World_map_-_low_resolution.svg');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      min-height: 100vh;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      padding: 15px;
      overflow-y: auto;
      position: relative;
      background-blend-mode: multiply;
      background-color: rgba(0,0,0,0.7);
    }

    #languageTable {
      position: fixed;
      top: 15px;
      left: 15px;
      background: rgba(0,0,0,0.6);
      border-radius: 10px;
      user-select: none;
      font-weight: 600;
      font-size: 0.9rem;
      border-collapse: collapse;
      width: 140px;
      z-index: 1000;
      margin-bottom: 10px;
    }
    #languageTable td {
      padding: 6px 10px;
      cursor: pointer;
      color: #ddd;
      text-align: center;
      border: none;
    }
    #languageTable td.selected {
      background: #ff6f61;
      color: white;
      border-radius: 6px;
    }
    #languageTable tr:hover td:not(.selected) {
      background: rgba(255, 255, 255, 0.1);
    }

    #app {
      background: rgba(0, 0, 0, 0.75);
      border-radius: 15px;
      width: 100%;
      max-width: 400px;
      padding: 20px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.4);
      margin-left: 180px;
      margin-bottom: 40px;
      display: flex;
      flex-direction: column;
      min-height: 90vh;
      max-height: 90vh;
    }
    h1, h2 {
      text-align: center;
      margin-bottom: 1rem;
      font-weight: 700;
      letter-spacing: 1px;
      user-select: none;
    }
    label {
      display: block;
      margin-bottom: 0.25rem;
      font-weight: 600;
      user-select: none;
    }
    input[type="text"],
    textarea {
      width: 100%;
      padding: 10px;
      border-radius: 8px;
      border: none;
      margin-bottom: 1rem;
      font-size: 1rem;
      font-family: inherit;
      resize: vertical;
    }
    textarea {
      min-height: 60px;
    }
    .checkbox-group, .link-table {
      margin-bottom: 1rem;
      user-select: none;
    }
    .link-table {
      border-collapse: collapse;
      width: 100%;
      table-layout: fixed;
      user-select: none;
      color: #ddd;
    }
    .link-table td {
      border: 1px solid rgba(255,255,255,0.3);
      padding: 10px;
      text-align: center;
      cursor: pointer;
      border-radius: 8px;
      transition: background-color 0.3s ease;
      font-weight: 600;
      user-select: none;
      color: #ddd;
      user-select: none;
    }
    .link-table td:hover {
      text-decoration: underline;
    }
    .link-table td#subscribeCell {
      background-color: #bf1e1e; /* deep red */
    }
    .link-table td#subscribeCell:hover:not(.selected) {
      background-color: #ff3b2f;
      color: white;
    }
    .link-table td#discordCell {
      background-color: #6f3f8f; /* purple */
    }
    .link-table td#discordCell:hover:not(.selected) {
      background-color: #9955cc;
      color: white;
    }
    .link-table td.selected {
      filter: brightness(0.9);
      cursor: default;
      text-decoration: none;
      color: white !important;
    }
    button {
      width: 100%;
      padding: 12px 0;
      border: none;
      border-radius: 10px;
      background-color: #ff6f61;
      color: white;
      font-weight: 700;
      font-size: 1.1rem;
      cursor: pointer;
      transition: background-color 0.3s ease;
      user-select: none;
    }
    button:disabled {
      background-color: #999;
      cursor: not-allowed;
    }
    button:hover:not(:disabled) {
      background-color: #ff3b2f;
    }
    .message {
      margin-top: 1rem;
      text-align: center;
      font-weight: 600;
      min-height: 24px;
    }
    .footer-links {
      margin-top: 10px;
      text-align: center;
      font-size: 0.9rem;
      user-select: none;
    }
    .footer-links a {
      color: #ffd1d0;
      text-decoration: none;
      font-weight: 600;
      margin: 0 6px;
      display: inline-block;
      max-width: 140px;
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;
      vertical-align: middle;
    }
    .footer-links a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <table id="languageTable" role="tablist" aria-label="Menu Bahasa / Language menu">
    <tr>
      <td id="langId" role="tab" aria-selected="true" tabindex="0" class="selected">Bahasa Indonesia</td>
      <td id="langEn" role="tab" aria-selected="false" tabindex="-1">English</td>
    </tr>
  </table>

  <div id="app" role="main" tabindex="-1">
    <h1 id="title">Formulir Pendaftaran Negara fiksi terbaru</h1>

    <form id="countryForm" novalidate>
      <label for="creatorName" id="labelCreatorName">Nama Pembuat</label>
      <input type="text" id="creatorName" name="creatorName" autocomplete="off" required placeholder="Masukkan nama pembuat" aria-required="true" />

      <label for="countryName" id="labelCountryName">Nama Negara</label>
      <input type="text" id="countryName" name="countryName" autocomplete="off" required placeholder="Masukkan nama negaranya" aria-required="true" />

      <label for="area" id="labelArea">Luas Wilayah</label>
      <input type="text" id="area" name="area" required placeholder="Contoh: 1000 km²" aria-required="true" />

      <label for="population" id="labelPopulation">Populasi</label>
      <input type="text" id="population" name="population" required placeholder="Contoh: 1 juta" aria-required="true" />

      <label for="capital" id="labelCapital">Ibu Kota</label>
      <input type="text" id="capital" name="capital" required placeholder="Masukkan ibu kota" aria-required="true" />

      <label for="language" id="labelLanguage">Bahasa Resmi</label>
      <input type="text" id="language" name="language" required placeholder="Masukkan bahasa resmi" aria-required="true" />

      <label for="currency" id="labelCurrency">Mata Uang</label>
      <input type="text" id="currency" name="currency" required placeholder="Masukkan mata uang" aria-required="true" />

      <label for="government" id="labelGovernment">Sistem Pemerintahan</label>
      <input type="text" id="government" name="government" required placeholder="Masukkan sistem pemerintahan" aria-required="true" />

      <label for="economy" id="labelEconomy">Ekonomi</label>
      <input type="text" id="economy" name="economy" required placeholder="Deskripsikan ekonomi singkat" aria-required="true" />

      <label for="history" id="labelHistory">Sejarah</label>
      <textarea id="history" name="history" required placeholder="Cerita sejarah singkat" aria-required="true"></textarea>

      <label for="culture" id="labelCulture">Budaya</label>
      <textarea id="culture" name="culture" required placeholder="Cerita budaya singkat" aria-required="true"></textarea>

      <table class="link-table" role="group" aria-label="Pilihan subscribe atau join">
        <tr>
          <td id="subscribeCell" tabindex="0" role="button" aria-pressed="false">Subscribe Channel</td>
          <td id="discordCell" tabindex="0" role="button" aria-pressed="false">Join Discord</td>
        </tr>
      </table>

      <input type="hidden" id="sendOption" name="sendOption" value="">

      <div class="footer-links" id="footerLinks" aria-label="Link sosial" style="margin-bottom:14px;">
        <a href="https://www.youtube.com/@FictionCountry-History210" target="_blank" rel="noopener noreferrer" id="youtubeLink" title="Subscribe YouTube Channel">YouTube Channel</a> |
        <a href="https://discord.gg/YYz7GB4x" target="_blank" rel="noopener noreferrer" id="discordLink" title="Join Discord Server">Discord Server</a>
      </div>

      <button type="submit" id="submitBtn" disabled>Kirim Data</button>
    </form>
    <p class="message" aria-live="polite" id="formMessage"></p>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/emailjs-com@3/dist/email.min.js"></script>
  <script>
    (function() {
      'use strict';

      emailjs.init('Q5lQIJmB1pkdeat79'); // Replace with your EmailJS user ID

      const langTexts = {
        id: {
          title: "Formulir Pendaftaran Negara fiksi terbaru",
          labelCreatorName: "Nama Pembuat",
          labelCountryName: "Nama Negara",
          labelArea: "Luas Wilayah",
          labelPopulation: "Populasi",
          labelCapital: "Ibu Kota",
          labelLanguage: "Bahasa Resmi",
          labelCurrency: "Mata Uang",
          labelGovernment: "Sistem Pemerintahan",
          labelEconomy: "Ekonomi",
          labelHistory: "Sejarah",
          labelCulture: "Budaya",
          labelSubscribe: "Subscribe channel YouTube",
          labelDiscord: "Join Discord",
          sendOptionsDesc: "Sebelum mengirim, pilih salah satu opsi:",
          submitBtn: "Kirim Data",
          youtubeLink: "https://www.youtube.com/@FictionCountry-History210",
          discordLink: "https://discord.gg/YYz7GB4x",
          placeholderCreatorName: "Masukkan nama pembuat",
          placeholderCountryName: "Masukkan nama negaranya",
          placeholderArea: "Contoh: 1000 km²",
          placeholderPopulation: "Contoh: 1 juta",
          placeholderCapital: "Masukkan ibu kota",
          placeholderLanguage: "Masukkan bahasa resmi",
          placeholderCurrency: "Masukkan mata uang",
          placeholderGovernment: "Masukkan sistem pemerintahan",
          placeholderEconomy: "Deskripsikan ekonomi singkat",
          placeholderHistory: "Cerita sejarah singkat",
          placeholderCulture: "Cerita budaya singkat",
          checkOptionRequired: "Silakan pilih minimal satu opsi: Subscribe channel YouTube atau Join Discord.",
          formSuccess: "Data Anda telah berhasil dikirim terima kasih!",
          formError: "Terjadi kesalahan saat mengirim data, coba lagi nanti."
        },
        en: {
          title: "Create Your Fictional Country",
          labelCreatorName: "Creator Name",
          labelCountryName: "Country Name",
          labelArea: "Area",
          labelPopulation: "Population",
          labelCapital: "Capital City",
          labelLanguage: "Official Language",
          labelCurrency: "Currency",
          labelGovernment: "Government System",
          labelEconomy: "Economy",
          labelHistory: "History",
          labelCulture: "Culture",
          labelSubscribe: "Subscribe to YouTube channel",
          labelDiscord: "Join Discord",
          sendOptionsDesc: "Before sending, please select one option:",
          submitBtn: "Send Data",
          youtubeLink: "https://www.youtube.com/@FictionCountry-History210",
          discordLink: "https://discord.gg/YYz7GB4x",
          placeholderCreatorName: "Enter creator name",
          placeholderCountryName: "Enter country name",
          placeholderArea: "Example: 1000 km²",
          placeholderPopulation: "Example: 1 million",
          placeholderCapital: "Enter capital city",
          placeholderLanguage: "Enter official language",
          placeholderCurrency: "Enter currency",
          placeholderGovernment: "Enter government system",
          placeholderEconomy: "Briefly describe economy",
          placeholderHistory: "Briefly describe history",
          placeholderCulture: "Briefly describe culture",
          checkOptionRequired: "Please select at least one option: Subscribe to YouTube channel or Join Discord.",
          formSuccess: "Your data has been sent successfully, thank you!",
          formError: "An error occurred while sending, please try again later."
        }
      };

      const elements = {
        langId: document.getElementById('langId'),
        langEn: document.getElementById('langEn'),
        title: document.getElementById('title'),
        labelCreatorName: document.getElementById('labelCreatorName'),
        labelCountryName: document.getElementById('labelCountryName'),
        labelArea: document.getElementById('labelArea'),
        labelPopulation: document.getElementById('labelPopulation'),
        labelCapital: document.getElementById('labelCapital'),
        labelLanguage: document.getElementById('labelLanguage'),
        labelCurrency: document.getElementById('labelCurrency'),
        labelGovernment: document.getElementById('labelGovernment'),
        labelEconomy: document.getElementById('labelEconomy'),
        labelHistory: document.getElementById('labelHistory'),
        labelCulture: document.getElementById('labelCulture'),
        labelSubscribe: document.getElementById('labelSubscribe'),
        labelDiscord: document.getElementById('labelDiscord'),
        sendOptionsDesc: document.getElementById('sendOptionsDesc'),
        submitBtn: document.getElementById('submitBtn'),
        youtubeLink: document.getElementById('youtubeLink'),
        discordLink: document.getElementById('discordLink'),
        subscribeCell: document.getElementById('subscribeCell'),
        discordCell: document.getElementById('discordCell'),
        sendOptionInput: document.getElementById('sendOption'),
        creatorName: document.getElementById('creatorName'),
        countryName: document.getElementById('countryName'),
        area: document.getElementById('area'),
        population: document.getElementById('population'),
        capital: document.getElementById('capital'),
        language: document.getElementById('language'),
        currency: document.getElementById('currency'),
        government: document.getElementById('government'),
        economy: document.getElementById('economy'),
        history: document.getElementById('history'),
        culture: document.getElementById('culture'),
        countryForm: document.getElementById('countryForm'),
        formMessage: document.getElementById('formMessage')
      };

      let currentLang = 'id';

      function updateLangSelectionUI() {
        if (currentLang === 'id') {
          elements.langId.classList.add('selected');
          elements.langId.setAttribute('aria-selected', 'true');
          elements.langId.tabIndex = 0;
          elements.langEn.classList.remove('selected');
          elements.langEn.setAttribute('aria-selected', 'false');
          elements.langEn.tabIndex = -1;
        } else {
          elements.langEn.classList.add('selected');
          elements.langEn.setAttribute('aria-selected', 'true');
          elements.langEn.tabIndex = 0;
          elements.langId.classList.remove('selected');
          elements.langId.setAttribute('aria-selected', 'false');
          elements.langId.tabIndex = -1;
        }
      }

      function switchLanguage(lang) {
        currentLang = lang;
        const t = langTexts[lang];
        document.documentElement.lang = lang;
        elements.title.textContent = t.title;
        elements.labelCreatorName.textContent = t.labelCreatorName;
        elements.labelCountryName.textContent = t.labelCountryName;
        elements.labelArea.textContent = t.labelArea;
        elements.labelPopulation.textContent = t.labelPopulation;
        elements.labelCapital.textContent = t.labelCapital;
        elements.labelLanguage.textContent = t.labelLanguage;
        elements.labelCurrency.textContent = t.labelCurrency;
        elements.labelGovernment.textContent = t.labelGovernment;
        elements.labelEconomy.textContent = t.labelEconomy;
        elements.labelHistory.textContent = t.labelHistory;
        elements.labelCulture.textContent = t.labelCulture;
        elements.labelSubscribe.textContent = t.labelSubscribe;
        elements.labelDiscord.textContent = t.labelDiscord;
        elements.sendOptionsDesc.textContent = t.sendOptionsDesc;
        elements.submitBtn.textContent = t.submitBtn;
        elements.youtubeLink.href = t.youtubeLink;
        elements.discordLink.href = t.discordLink;
        elements.creatorName.placeholder = t.placeholderCreatorName;
        elements.countryName.placeholder = t.placeholderCountryName;
        elements.area.placeholder = t.placeholderArea;
        elements.population.placeholder = t.placeholderPopulation;
        elements.capital.placeholder = t.placeholderCapital;
        elements.language.placeholder = t.placeholderLanguage;
        elements.currency.placeholder = t.placeholderCurrency;
        elements.government.placeholder = t.placeholderGovernment;
        elements.economy.placeholder = t.placeholderEconomy;
        elements.history.placeholder = t.placeholderHistory;
        elements.culture.placeholder = t.placeholderCulture;
        updateLangSelectionUI();
      }

      elements.langId.addEventListener('click', () => switchLanguage('id'));
      elements.langId.addEventListener('keydown', e => { if(e.key === 'Enter' || e.key === ' ') { e.preventDefault(); switchLanguage('id'); }});
      elements.langEn.addEventListener('click', () => switchLanguage('en'));
      elements.langEn.addEventListener('keydown', e => { if(e.key === 'Enter' || e.key === ' ') { e.preventDefault(); switchLanguage('en'); }});

      // Link click handlers for subscribe/join discord
      function handleLinkClick(option) {
        if (option === 'subscribe') {
          window.open(elements.youtubeLink.href, '_blank', 'noopener');
          setSelectedOption('subscribe');
        } else if (option === 'discord') {
          window.open(elements.discordLink.href, '_blank', 'noopener');
          setSelectedOption('discord');
        }
      }

      function setSelectedOption(option) {
        elements.sendOptionInput.value = option;
        elements.submitBtn.disabled = false;
        if(option === 'subscribe') {
          elements.subscribeCell.classList.add('selected');
          elements.subscribeCell.setAttribute('aria-pressed','true');
          elements.discordCell.classList.remove('selected');
          elements.discordCell.setAttribute('aria-pressed','false');
        } else if(option === 'discord') {
          elements.discordCell.classList.add('selected');
          elements.discordCell.setAttribute('aria-pressed','true');
          elements.subscribeCell.classList.remove('selected');
          elements.subscribeCell.setAttribute('aria-pressed','false');
        }
      }

      function isFormValid() {
        const requiredFields = [
          elements.creatorName,
          elements.countryName,
          elements.area,
          elements.population,
          elements.capital,
          elements.language,
          elements.currency,
          elements.government,
          elements.economy,
          elements.history,
          elements.culture
        ];
        let valid = true;
        for (const field of requiredFields) {
          if (!field.value.trim()) {
            valid = false;
            break;
          }
        }
        if (!elements.sendOptionInput.value) {
          valid = false;
        }
        return valid;
      }

      elements.subscribeCell.addEventListener('click', () => handleLinkClick('subscribe'));
      elements.subscribeCell.addEventListener('keydown', e => { if(e.key==='Enter' || e.key===' ') { e.preventDefault(); handleLinkClick('subscribe'); }});
      elements.discordCell.addEventListener('click', () => handleLinkClick('discord'));
      elements.discordCell.addEventListener('keydown', e => { if(e.key==='Enter' || e.key===' ') { e.preventDefault(); handleLinkClick('discord'); }});

      elements.countryForm.addEventListener('submit', function(event) {
        event.preventDefault();
        elements.formMessage.textContent = '';
        elements.formMessage.style.color = '';

        if (!isFormValid()) {
          elements.formMessage.textContent = langTexts[currentLang].checkOptionRequired;
          elements.formMessage.style.color = '#ff6f61';
          return;
        }
        const formData = {
          creatorName: elements.creatorName.value.trim(),
          countryName: elements.countryName.value.trim(),
          area: elements.area.value.trim(),
          population: elements.population.value.trim(),
          capital: elements.capital.value.trim(),
          language: elements.language.value.trim(),
          currency: elements.currency.value.trim(),
          government: elements.government.value.trim(),
          economy: elements.economy.value.trim(),
          history: elements.history.value.trim(),
          culture: elements.culture.value.trim(),
          sendOption: elements.sendOptionInput.value === 'subscribe' ? langTexts[currentLang].labelSubscribe : langTexts[currentLang].labelDiscord
        };

        elements.submitBtn.disabled = true;
        elements.submitBtn.textContent = (currentLang==='id') ? 'Mengirim...' : 'Sending...';

        // Prepare email params
        const emailParams = {
          to_email: 'your-email@gmail.com', // TODO: replace in EmailJS template or settings
          creator_name: formData.creatorName,
          country_name: formData.countryName,
          area: formData.area,
          population: formData.population,
          capital: formData.capital,
          language: formData.language,
          currency: formData.currency,
          government: formData.government,
          economy: formData.economy,
          history: formData.history,
          culture: formData.culture,
          sent_via: formData.sendOption
        };

        emailjs.send('service', 'template', emailParams)
          .then(() => {
            elements.formMessage.textContent = langTexts[currentLang].formSuccess;
            elements.formMessage.style.color = '#4caf50';
            elements.countryForm.reset();
            elements.submitBtn.textContent = langTexts[currentLang].submitBtn;
            elements.submitBtn.disabled = true;
            elements.sendOptionInput.value = '';
            elements.subscribeCell.classList.remove('selected');
            elements.discordCell.classList.remove('selected');
            elements.subscribeCell.setAttribute('aria-pressed','false');
            elements.discordCell.setAttribute('aria-pressed','false');
          }, (error) => {
            console.error('FAILED...', error);
            elements.formMessage.textContent = langTexts[currentLang].formError;
            elements.formMessage.style.color = '#ff6f61';
            elements.submitBtn.textContent = langTexts[currentLang].submitBtn;
            elements.submitBtn.disabled = false;
          });
      });

      switchLanguage(currentLang);
    })();
  </script>
</body>
</html>

