# 🏗 Sovereign AI Architect: Course Repository (2026)

Добро пожаловать в официальный репозиторий практического курса **"Применение ИИ в разработке ПО: От Copilot к Автономным Агентам"**.

Здесь вы будете выполнять лабораторные работы, строить RAG-пайплайны, проектировать графы агентов и сдавать домашние задания.

---

## 📚 Структура курса

Репозиторий разбит на модули. В каждой папке находится `README.md` с заданием и стартовый код.

| Модуль | Тема | Статус | Дедлайн |
| :--- | :--- | :--- | :--- |
| **[Module 1](./module_01)** | Экосистема и Промпт-инжиниринг (DSPy) | ✅ Открыт | --.--.2026 |
| **[Module 2](./module_02)** | **The Engine: Hybrid RAG & Logic** | 🚀 **Active** | --.--.2026 |
| **[Module 3](./module_03)** | Agent Architecture (LangGraph) | 🔒 Скоро | --.--.2026 |
| **[Module 4](./module_04)** | LLMOps & Observability | 🔒 Скоро | --.--.2026 |
| **[Final Project](./final_project)** | Sovereign Code Oracle | 🔒 Скоро | --.--.2026 |

---

## 🛠 Технический стек (Laptop-Ready)

Мы не используем платные API (OpenAI/Claude). Весь курс проходят на локальном или Google Colab оборудовании.

**Требования:**
*   **OS:** Linux / macOS / Windows (WSL2)
*   **Python:** 3.11+
*   **RAM:** Минимум 16GB (для запуска квантованных моделей 7B).
*   **GPU:** Желательно NVIDIA (6GB+ VRAM) или Apple Silicon (M1/M2/M3).

**Инструментарий:**
1.  **[Ollama](https://ollama.com)** — локальный запуск моделей.
2.  **LangGraph** — оркестрация агентов.
3.  **Qdrant / LanceDB** — векторный поиск.
4.  **Arize Phoenix** — трейсинг и отладка.

---

## 🚀 Как сдавать домашние задания (Workflow)

Мы работаем по классическому Open Source процессу через **Fork & Pull Request**.

### Шаг 1. Подготовка
1. Сделайте **Fork** этого репозитория к себе в профиль.
2. Склонируйте свой форк:
   ```bash
   git clone https://github.com/YOUR_USERNAME/sovereign-ai-course.git
   cd sovereign-ai-course
   ```
3. Настройте окружение (рекомендуется `uv` или `poetry`, но `venv` тоже ок):
   ```bash
   python -m venv venv
   source venv/bin/activate  # или venv\Scripts\activate на Windows
   pip install -r requirements.txt
   ```

### Шаг 2. Выполнение задания
1. Перейдите в папку модуля (например, `cd module_02`).
2. Создайте ветку для задания по шаблону: `submission/module-N-<фамилия>`.
   ```bash
   git checkout -b submission/module-02-ivanov
   ```
3. Выполните задания в ноутбуке `.ipynb` или в `.py` файлах.
4. **Важно:** Сохраните результаты выполнения ячеек (output) в ноутбуках, чтобы преподаватель видел логи (Traceback, ответы LLM) без перезапуска.

### Шаг 3. Отправка (Submit)
1. Закоммитьте и запушьте изменения в **свой** форк:
   ```bash
   git add .
   git commit -m "feat: completed module 2 tasks"
   git push origin submission/module-02-ivanov
   ```
2. Зайдите на GitHub в свой репозиторий и нажмите **Compare & pull request**.
3. В описании PR укажите:
   *   Какие задачи выполнены полностью.
   *   С какими трудностями столкнулись.
   *   (Опционально) Ссылку на трейс в Phoenix, если задание требовало отладки.
4. Укажите преподавателя (@AndreyNosovAI - *пример*) в ревьюерах.

---

## ✅ Критерии приемки (Definition of Done)

Ваша работа будет принята, если:

1.  **Код работает:** Логика воспроизводима. Если нужен `.env` файл, приложите `.env.example`.
2.  **Локальность:** Код НЕ обращается к OpenAI/Anthropic. Используется только `ChatOllama` или `LlamaCpp`.
3.  **Доказательства:** В ноутбуках сохранены выводы (Outputs). Если задание требовало CLI-утилит — приложены скриншоты консоли.
4.  **Чистота:** Код структурирован, функции имеют Type Hints (аннотации типов) и Docstrings.

---

## 🆘 FAQ / Troubleshooting

**Q: У меня слабый ноутбук, Ollama тормозит.**
A: Используйте **Google Colab (T4 GPU)**. В папке каждого модуля есть ссылка на Colab-версию задания. Выполните его там, скачайте `.ipynb` и залейте в репозиторий.

**Q: Модель галлюцинирует и не выдает JSON.**
A: Это нормально для SLM (Small Language Models). Реализуйте **Fallback-механизм** (try/except блок), как мы разбирали на лекции. Это часть задания.

**Q: Arize Phoenix не открывается.**
A: Убедитесь, что порт `6006` свободен. Если работаете в Colab, используйте туннелирование или смотрите логи в консоли.

---

Happy Coding & Building Sovereign AI! 🤖🏗️
```

### Что еще нужно сделать:
1.  Создать в корне файл `requirements.txt` с базовыми зависимостями:
    ```text
    langchain==0.1.0
    langchain-ollama
    langchain-community
    langgraph
    lancedb
    networkx
    arize-phoenix
    qdrant-client
    sentence-transformers
    jupyter
    pytest
    ```
2.  Создать файл `.gitignore` (чтобы студенты не пушили лишнее):
    ```text
    __pycache__/
    *.pyc
    .env
    venv/
    .ipynb_checkpoints/
    *.log
    phoenix-data/
    lancedb_data/
    ```
