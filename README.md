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
