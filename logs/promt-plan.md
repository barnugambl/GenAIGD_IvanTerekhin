
**Направление:** Локация — `Архив Памяти` 

---

## Версия 1: Базовый / Установочный кадр

**Задача генерации**  
Создать чистый, архитектурно-выразительный общий план Архива. Акцент на масштабе, пространстве и функциональности хранилища. Используется как референс для левел-дизайна и стартового экрана.

**Positive Prompt — t5xxl**  
`A vast, minimalist interior of a conceptual memory archive. Brutalist concrete platforms and translucent glass walkways float in a soft, luminous mist. Hundreds of faintly glowing crystalline shards drift slowly in zero gravity. Clean geometric lines dominate the composition, large areas of negative space. Volumetric lighting from above, muted cool blue and warm amber tones. Cinematic wide shot, photorealistic concept art style, highly detailed architecture.`

**Positive Prompt — clip_l**  
`archive hub, memory crystals, brutalist architecture, volumetric lighting, minimalist concept art, wide angle, cinematic`

**Критерии отбора**  
Читаемая перспектива и пропорции платформ  
Преобладание пустого пространства (negative space) не менее 40% кадра  
Спокойная, приглушенная палитра без кислотных акцентов  
Отсутствие лишних декоративных элементов

**Краткий комментарий**  
Базовая версия. `t5xxl` задаёт детальное атмосферное описание, `clip_l` фиксирует ключевые визуальные маркеры. Версия для "чистого" состояния Архива до распада.

---

##  Версия 2: Атмосферный / Состояние распада

**Задача генерации**  
Визуализировать механику "распада памяти" (таймер 72 часа). Показать энтропию, нестабильность данных и сюрреалистичную тревожность без ухода в хоррор.

**Positive Prompt — t5xxl**  
`Interior of a decaying memory archive. Concrete walkways show subtle stress cracks and floating dust motes. Several memory shards flicker with digital glitch artifacts, chromatic aberration, and soft motion blur. Volumetric light breaks through fractured glass panels, casting long, diffused shadows. Surreal atmosphere inspired by restrained Beksiński aesthetics — melancholic, not horrifying. Wide-angle composition, desaturated muted tones, slow sense of entropy, cinematic lighting, photorealistic.`

**Positive Prompt — clip_l**  
`decaying archive, glitching crystals, cracked concrete, volumetric dust, Beksiński style, desaturated, cinematic, surreal atmosphere`

**Критерии отбора**  
Наличие эффектов "распада" (трещины, глитч, пыль, размытие)  
Сохранение читаемости архитектуры и композиции  
Атмосфера тревоги и увядания, но без пугающих или агрессивных элементов  
Цветовая палитра смещена в холодные/серые тона

**Краткий комментарий**  
Версия с акцентом на нарратив: распад = прогресс игры. `t5xxl` описывает состояние среды, `clip_l` усиливает ключевые визуальные маркеры распада. Отличается от Версии 1 добавлением энтропии и сдвигом палитры.

---

## Версия 3: Камерный / Фокус на объекте

**Задача генерации**  
Крупный план "осколка памяти" (memory shard) — ключевого пропса игры. Показать, как внутри кристалла застыл фрагмент воспоминания. Используется для иконок, интерфейса и кат-сцен.

**t5 promt**  
`Extreme close-up of a translucent crystalline shard floating in soft mist. Inside the crystal, a faint frozen scene is visible: a blurred human silhouette reaching out. The shard surface shows subtle internal fractures and light refraction. Soft rim lighting highlights the edges, shallow depth of field blurs the background into smooth bokeh. Macro photography style, photorealistic, muted tones with a single warm accent from the memory glow.`

**clip promt**  
`memory shard, crystal close-up, frozen memory inside, macro photography, rim lighting, shallow depth of field, photorealistic prop`

**Критерии отбора**  
Чёткий фокус на одном объекте (осколок)  
Внутри кристалла различим намёк на сцену/силуэт  
Красивая работа со светом (преломление, блики, боке)  
Стиль — фотореалистичный макро-пропс, не иллюстрация

**Краткий комментарий**  
Версия для пропса/иконки. `t5xxl` детально описывает материал и свет, `clip_l` фиксирует тип кадра (macro, close-up). Отличается от предыдущих масштабом и фокусом на одном объекте.

---

## 🔁 План итераций

| Итерация | Что меняю | Цель |
|----------|-----------|------|
| 1 | Базовые промпты выше | Получить 3 референса по ключевым визуальным направлениям |
| 2 | Добавить `guidance=4.5` и `guidance=2.5` | Проверить, как меняется "послушность" модели промпту |
| 3 | В `clip_l` добавить стиль-референс (`Zdzisław Beksiński style`) | Усилить художественную консистентность |
| 4 | Протестировать `IP-Adapter` с референс-изображением | Зафиксировать форму осколка/архитектуру для серийной генерации |