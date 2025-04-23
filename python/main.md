# 🐍 MeynDev Python Guidelines

Добро пожаловать в гайд по настройке Python-проектов в команде **MeynDev**! Ниже собраны рекомендуемые инструменты и шаги, которые помогут тебе быстро и удобно стартануть новый проект 🚀

---

## 🔧 Инструменты, которые мы используем

| 💡 Что делает          | 🛠 Инструмент                                                                                                                                    | 🧠 Для чего нужен                            |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| 📦 Управление проектом | [![uv](https://img.shields.io/badge/uv-DE5FE9?style=for-the-badge&logo=uv&logoColor=white)](https://github.com/astral-sh/uv)                     | Виртуальные окружения и зависимости          |
| ✨ Стиль кода           | [![ruff](https://img.shields.io/badge/ruff-D7FF64?style=for-the-badge&logo=ruff&logoColor=black)](https://github.com/astral-sh/ruff)             | Линтинг, автоформатирование и стиль кода     |
| ✅ Тестирование         | [![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)](https://pytest.org)                      | Написание и запуск тестов                    |
| 🏗 Компиляция          | [![Nuitka](https://img.shields.io/badge/nuitka-3776AB?style=for-the-badge&logo=nuitka&logoColor=white)](https://nuitka.net)                      | Компиляция Python в нативные бинарники       |
| 🔍 Проверка типов      | [![Pyright](https://img.shields.io/badge/Pyright-C3C38F?style=for-the-badge&logo=pyright&logoColor=white)](https://github.com/microsoft/pyright) | Быстрая и лёгкая проверка типов              |
| 🪝 Прехуки             | [![pre-commit](https://img.shields.io/badge/pre--commit-FAB040?style=for-the-badge&logo=pre-commit&logoColor=black)](https://pre-commit.com)     | Автоматизация проверки качества при коммитах |

---

## 🚀 Как создать новый проект

1. **Инициализируй проект с помощью `uv`:**

   ```bash
   uv init ZapFiles-rewritten && cd ZapFiles-rewritten
   ```

2. **Создай и активируй виртуальное окружение:**

   - 🐧 **Linux:**
     ```bash
     uv venv && source .venv/bin/activate
     ```

   - 🪟 **Windows:**
     ```bash
     uv venv && .venv\Scripts\activate
     ```

3. **Установи инструменты для разработки:**

   ```bash
   uv add pre-commit ruff "pyright[nodejs]" --dev
   ```

4. **Скачай базовую конфигурацию pre-commit:**

   ```bash
   curl -L -o .pre-commit-config.yaml https://raw.githubusercontent.com/MeynDev/.guidelines/main/python/.pre-commit-config.yaml
   ```

5. **Обнови хуки и установи их:**

   ```bash
   pre-commit autoupdate && pre-commit install
   ```

6. **Проинициализируй git-репозиторий:**

   ```bash
   git add . && git commit -m "🚀 Initialized project"
   ```
