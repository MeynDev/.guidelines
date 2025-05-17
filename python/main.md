# 🐍 MeynDev Python Guidelines

Привет 👋  
Добро пожаловать в гайд по настройке Python-проектов в команде **MeynDev**! Здесь ты найдёшь список рекомендуемых инструментов и подробную пошаговую инструкцию для запуска нового проекта как на Linux/macOS, так и на Windows (PowerShell) 🚀

---

## 🔧 Инструменты, которые мы используем

| 💡 Назначение           | 🛠 Инструмент                                                                                                                                    | 🧠 Зачем нужен                                 |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| 📦 Управление проектом  | [![uv](https://img.shields.io/badge/uv-DE5FE9?style=for-the-badge&logo=uv&logoColor=white)](https://github.com/astral-sh/uv)                     | Управление зависимостями и виртуальным окружением |
| ✨ Стиль кода            | [![ruff](https://img.shields.io/badge/ruff-D7FF64?style=for-the-badge&logo=ruff&logoColor=black)](https://github.com/astral-sh/ruff)             | Линтинг, автоформатирование и проверка стиля     |
| ✅ Тестирование          | [![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)](https://pytest.org)                      | Написание и выполнение тестов                   |
| 🏗 Компиляция            | [![Nuitka](https://img.shields.io/badge/nuitka-3776AB?style=for-the-badge&logo=nuitka&logoColor=white)](https://nuitka.net)                      | Компиляция Python-кода в нативные бинарники     |
| 🔍 Проверка типов        | [![Pyright](https://img.shields.io/badge/Pyright-C3C38F?style=for-the-badge&logo=pyright&logoColor=white)](https://github.com/microsoft/pyright) | Быстрая статическая проверка типов              |
| 🪝 Прехуки               | [![pre-commit](https://img.shields.io/badge/pre--commit-FAB040?style=for-the-badge&logo=pre-commit&logoColor=black)](https://pre-commit.com)     | Автоматическая проверка качества при коммитах   |

---

## 🐧 Установка на Linux/macOS (bash/zsh)

1. **Создай проект:**

   ```bash
   uv init project-name && cd project-name
   ```

2. **Создай и активируй виртуальное окружение:**

   ```bash
   uv venv && source .venv/bin/activate
   ```

3. **Установи инструменты разработки:**

   ```bash
   uv add --dev pre-commit ruff "pyright[nodejs]"
   ```

4. **Добавь базовую конфигурацию pre-commit:**

   ```bash
   curl -L -o .pre-commit-config.yaml https://raw.githubusercontent.com/MeynDev/.guidelines/main/python/.pre-commit-config.yaml
   ```

5. **Обнови и установи хуки:**

   ```bash
   pre-commit autoupdate
   pre-commit install
   ```

6. **Инициализируй Git и сделай первый коммит:**

   ```bash
   git init
   git add .
   git commit -m "🚀 Initial project setup"
   ```

---

## 🪟 Установка на Windows (PowerShell)

1. **Создай проект:**

   ```powershell
   uv init project-name; Set-Location project-name
   ```

2. **Создай и активируй виртуальное окружение:**

   ```powershell
   uv venv; .\.venv\Scripts\Activate.ps1
   ```

3. **Установи инструменты разработки:**

   ```powershell
   uv add --dev pre-commit ruff "pyright[nodejs]"
   ```

4. **Добавь базовую конфигурацию pre-commit:**

   ```powershell
   Invoke-WebRequest -Uri https://raw.githubusercontent.com/MeynDev/.guidelines/main/python/.pre-commit-config.yaml -OutFile .pre-commit-config.yaml
   ```

5. **Обнови и установи хуки:**

   ```powershell
   pre-commit autoupdate
   pre-commit install
   ```

6. **Инициализируй Git и сделай первый коммит:**

   ```powershell
   git init
   git add .
   git commit -m "🚀 Initial project setup"
   ```

---

🎉 Всё готово! У тебя теперь есть чистый и современный Python-проект с единым стилем, типизацией и удобными инструментами. Удачи в разработке! 💪
