# 📊 Профессиональный анализ производительности PostgreSQL

> **DBA Report Generator v2.0** - Комплексный анализ базы данных

**Дата анализа**: 2026-01-22 23:04:45

---

## 📋 Executive Summary

- **Период мониторинга**: 60 минут
- **Проанализировано баз данных**: 3
- **Критических проблем**: 0
- **Предупреждений**: 0
- **Рекомендаций**: 0

🟢 **Статус**: База данных работает удовлетворительно

---

## ⏱️ Период мониторинга

| Параметр | Значение |
|----------|----------|
| **Начало** | `2026-01-22 05:40:02+03` |
| **Конец** | `2026-01-22 06:40:02+03` |
| **Длительность** | 60 минут |

---

## 🗄️ Общая статистика баз данных

### База данных: `microservices_db`

| Метрика | Значение |
|---------|----------|
| **Размер БД** | 983 GB |
| **Изменение размера** | 18 GB |
| **Cache Hit Ratio** | 99.32% |
| **Commits** | 10,585,922 |
| **Rollbacks** | 1,910 (0.02%) |
| **Deadlocks** |  |
| **Временные файлы** |  |

✅ **Проблем не обнаружено**

### База данных: `postgres`

| Метрика | Значение |
|---------|----------|
| **Размер БД** | 531 MB |
| **Изменение размера** | 112 kB |
| **Cache Hit Ratio** | 99.50% |
| **Commits** | 35,503 |
| **Rollbacks** | 130 (0.36%) |
| **Deadlocks** |  |
| **Временные файлы** |  |

✅ **Проблем не обнаружено**

### База данных: `Total`

| Метрика | Значение |
|---------|----------|
| **Размер БД** | 984 GB |
| **Изменение размера** | 18 GB |
| **Cache Hit Ratio** | 99.32% |
| **Commits** | 10,621,425 |
| **Rollbacks** | 2,040 (0.02%) |
| **Deadlocks** |  |
| **Временные файлы** |  |

✅ **Проблем не обнаружено**

---

## 🔥 Топ самых тяжелых запросов

*Анализ 10 запросов с наибольшим временем выполнения*

### 1. Query ID: `8324a69d74a295fd`

**SQL Preview:** `['WITH inserted_services_raw AS ( INSERT INTO "si_dbaccessor"."Services" ("Category", "Description",...`

| Параметр | Значение |
|----------|----------|
| **База данных** | microservices_db |
| **Пользователь** | si_dbaccessor |
| **Количество вызовов** | 583,143 |
| **Общее время выполнения** | 438350 мс |
| **Среднее время** | 0.75 мс |
| **Количество строк** | 583,143 |
| **Cache Hit Ratio** | 100.0% |

✅ **Запрос работает нормально**

---

### 2. Query ID: `47050f2c3d9c165c`

**SQL Preview:** `['with updated as ( update "Outbox" set status = 1, status_date = current_timestamp where 1 = 1 and ...`

| Параметр | Значение |
|----------|----------|
| **База данных** | microservices_db |
| **Пользователь** | si_dbaccessor |
| **Количество вызовов** | 100,368 |
| **Общее время выполнения** | 359980 мс |
| **Среднее время** | 3.59 мс |
| **Количество строк** | 583,025 |
| **Cache Hit Ratio** | 100.0% |

✅ **Запрос работает нормально**

---

### 3. Query ID: `11ae9084b8cb4ce1`

**SQL Preview:** `['WITH inserted_profile AS ( INSERT INTO "si_dbaccessor"."SubscriptionProfiles" ("Structure", "Msisd...`

| Параметр | Значение |
|----------|----------|
| **База данных** | microservices_db |
| **Пользователь** | si_dbaccessor |
| **Количество вызовов** | 583,113 |
| **Общее время выполнения** | 290690 мс |
| **Среднее время** | 0.50 мс |
| **Количество строк** | 583,113 |
| **Cache Hit Ratio** | 98.5% |

✅ **Запрос работает нормально**

---

### 4. Query ID: `f5d7110ec1695299`

**SQL Preview:** `['SELECT DISTINCT s."Id" FROM "si_dbaccessor"."Services" s JOIN "si_dbaccessor"."SubscriptionProfile...`

| Параметр | Значение |
|----------|----------|
| **База данных** | microservices_db |
| **Пользователь** | si_dbaccessor |
| **Количество вызовов** | 593,138 |
| **Общее время выполнения** | 234340 мс |
| **Среднее время** | 0.40 мс |
| **Количество строк** | 140 |
| **Cache Hit Ratio** | 81.6% |

**⚠️ Проблемы:**

- Низкий cache hit: 81.6%

**💡 Рекомендации:**

- Проверить индексы и статистику таблиц

---

### 5. Query ID: `1d7f9633e4c04dba`

**SQL Preview:** `['SELECT DISTINCT "SubscriptionProfileId" FROM si_dbaccessor."Services" WHERE "SubscriptionProfileId...`

| Параметр | Значение |
|----------|----------|
| **База данных** | microservices_db |
| **Пользователь** | si_dbaccessor |
| **Количество вызовов** | 583,233 |
| **Общее время выполнения** | 229800 мс |
| **Среднее время** | 0.39 мс |
| **Количество строк** | 93 |
| **Cache Hit Ratio** | 82.3% |

**⚠️ Проблемы:**

- Низкий cache hit: 82.3%

**💡 Рекомендации:**

- Проверить индексы и статистику таблиц

---

### 6. Query ID: `6d5cf0d935eb3cd`

**SQL Preview:** `['UPDATE "si_dbaccessor"."SubscriptionProfiles" SET "Structure" = $1::jsonb, "ChangeDate" = $2, "Ver...`

| Параметр | Значение |
|----------|----------|
| **База данных** | microservices_db |
| **Пользователь** | si_dbaccessor |
| **Количество вызовов** | 583,145 |
| **Общее время выполнения** | 186220 мс |
| **Среднее время** | 0.32 мс |
| **Количество строк** | 583,145 |
| **Cache Hit Ratio** | 99.5% |

✅ **Запрос работает нормально**

---

### 7. Query ID: `bba03f2349f3acef`

**SQL Preview:** `['insert into "Outbox" ( message, topic ) values ( $1, $2 ) returning id']`

| Параметр | Значение |
|----------|----------|
| **База данных** | microservices_db |
| **Пользователь** | si_dbaccessor |
| **Количество вызовов** | 583,144 |
| **Общее время выполнения** | 142680 мс |
| **Среднее время** | 0.24 мс |
| **Количество строк** | 583,144 |
| **Cache Hit Ratio** | 100.0% |

✅ **Запрос работает нормально**

---

### 8. Query ID: `ea478e299ed74530`

**SQL Preview:** `['UPDATE so_basket."Process" AS p SET "Status" = $5, "ResponseTime" = $1, "ResponseJson" = $2 WHERE ...`

| Параметр | Значение |
|----------|----------|
| **База данных** | microservices_db |
| **Пользователь** | so_basket |
| **Количество вызовов** | 596,898 |
| **Общее время выполнения** | 138310 мс |
| **Среднее время** | 0.23 мс |
| **Количество строк** | 596,898 |
| **Cache Hit Ratio** | 99.3% |

✅ **Запрос работает нормально**

---

### 9. Query ID: `7ac20be2003823dd`

**SQL Preview:** `['INSERT INTO so_storage."ServiceOrderSearch" ("PartitionId", "SearchField", "SearchValue", "Service...`

| Параметр | Значение |
|----------|----------|
| **База данных** | microservices_db |
| **Пользователь** | so_storage |
| **Количество вызовов** | 596,792 |
| **Общее время выполнения** | 128330 мс |
| **Среднее время** | 0.22 мс |
| **Количество строк** | 2,970,289 |
| **Cache Hit Ratio** | 100.0% |

✅ **Запрос работает нормально**

---

### 10. Query ID: `8e1c8dbc901b8bc8`

**SQL Preview:** `['INSERT INTO so_archive."ServiceOrderSearch" ("PartitionId", "SearchField", "SearchValue", "Service...`

| Параметр | Значение |
|----------|----------|
| **База данных** | microservices_db |
| **Пользователь** | so_archive |
| **Количество вызовов** | 4,157,615 |
| **Общее время выполнения** | 109640 мс |
| **Среднее время** | 0.03 мс |
| **Количество строк** | 4,157,615 |
| **Cache Hit Ratio** | 99.7% |

✅ **Запрос работает нормально**

---

## 📝 Статистика Write-Ahead Log (WAL)

| Метрика | Значение |
|---------|----------|
| **Количество записей** | 151,636,498 |
| **Full Page Images** | 3,321,271 |
| **Объем WAL** | 49617.57 MB (48.455 GB) |
| **Время записи** | 66.91 мс |
| **Время синхронизации** | 1374.27 мс |

**Скорость генерации WAL**: 826.96 MB/мин

⚠️ **Высокая скорость генерации WAL** - возможно много операций записи

### 📊 Топ-5 запросов по генерации WAL

*Запросы с наибольшим объемом Write-Ahead Log*

**1. Query ID:** `8324a69d74a295fd`

- **SQL Preview:** `['WITH inserted_services_raw AS ( INSERT INTO "si_...`
- **База данных:** microservices_db
- **Количество вызовов:** 583,143
- **Объем WAL:** 8746.72 MB — 17.5% от общего WAL

**2. Query ID:** `11ae9084b8cb4ce1`

- **SQL Preview:** `['WITH inserted_profile AS ( INSERT INTO "si_dbacc...`
- **База данных:** microservices_db
- **Количество вызовов:** 583,113
- **Объем WAL:** 6500.83 MB — 13.0% от общего WAL

**3. Query ID:** `16888b614ed8cf67`

- **SQL Preview:** `['INSERT INTO so_basket."ProcessStepsCompressed" (...`
- **База данных:** microservices_db
- **Количество вызовов:** 596,891
- **Объем WAL:** 4207.80 MB — 8.4% от общего WAL

**4. Query ID:** `636d820f2c906a61`

- **SQL Preview:** `['INSERT INTO so_archive."ServiceOrder" ("Id", "Pa...`
- **База данных:** microservices_db
- **Количество вызовов:** 595,899
- **Объем WAL:** 3210.61 MB — 6.4% от общего WAL

**5. Query ID:** `ea478e299ed74530`

- **SQL Preview:** `['UPDATE so_basket."Process" AS p SET "Status" = $...`
- **База данных:** microservices_db
- **Количество вызовов:** 596,898
- **Объем WAL:** 2948.03 MB — 5.9% от общего WAL


---

## 📋 Общие выводы и рекомендации

### ✅ Что работает хорошо

- Отличный cache hit ratio в БД `microservices_db`: 99.32%
- Отличный cache hit ratio в БД `postgres`: 99.50%
- Отличный cache hit ratio в БД `Total`: 99.32%
- Все таблицы имеют хороший Heap Cache Hit Ratio
- Нет проблем с Sequential Scans на больших таблицах

### 🔴 Критические проблемы

- **Экстремально высокая скорость WAL**: 827.0 MB/мин (норма < 100 MB/мин)

### 💡 Приоритетные рекомендации по оптимизации


#### 🟡 Средний приоритет

1. **Высокая генерация WAL**: 827.0 MB/мин - оптимизировать операции записи

---

## 📚 Методология и дополнительная информация

### 🔬 Критерии анализа

**Пороговые значения:**

- Cache Hit Ratio: ≥ 95%
- Heap Hit Ratio: ≥ 90%
- Index Hit Ratio: ≥ 95%
- Dead Tuples Ratio: ≤ 20%
- Sequential Scan Threshold: ≤ 100 для таблиц > 100 MB
- Query Mean Time: < 1000 мс
- WAL Generation Rate: < 100 MB/мин

### 📊 Анализируемые метрики

1. **Database Statistics**: Cache hit ratio, commits, rollbacks, deadlocks
2. **WAL Activity**: Generation rate, top WAL generators
3. **Query Performance**: Execution time, I/O wait, variance
4. **Table Health**: Bloat, dead tuples, vacuum/analyze status
5. **Index Usage**: Unused indexes, index cache hit ratio
6. **Memory Configuration**: shared_buffers, work_mem, effective_cache_size
7. **Buffer Management**: Buffer reuse, heap/index cache hit ratios
8. **Query Patterns**: Sequential scans, I/O-bound queries

### 🛠️ Инструменты

- **DBA Report Generator**: v2.0
- **Анализатор**: Python + pandas + openpyxl
- **Источник данных**: PostgreSQL pg_profile extension

---

*Отчет сгенерирован автоматически: 2026-01-22 23:04:45*

*На основе критериев профессионального DBA анализа PostgreSQL*
