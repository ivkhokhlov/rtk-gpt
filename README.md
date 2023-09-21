Видеокарты нужны для запуска нейронок локально, без отправки кода во внешние источники.
Самые популярные приложения на данный момент
# text-generation-webui

Локальный интерфейс взаимодействия нападобие ChatGPT с расширенным функционалом.

https://github.com/oobabooga/text-generation-webui
![image](https://github.com/ivkhokhlov/rtk-gpt/assets/58159018/14c0b5eb-286d-4670-a7ec-a9f6b5c1c7b4)

## Основные фичи text-generation-webui:
- **Gradio веб-интерфейс для больших языковых моделей**: Целью является стать аналогом AUTOMATIC1111/stable-diffusion-webui для генерации текста.
- **3 режима интерфейса**: По умолчанию (два столбца), блокнот и чат.
- **Множественные модели**: Поддерживает такие модели, как transformers, ExLlamaV2, CTransformers.
- **Выпадающее меню**: Для быстрого переключения между различными моделями.
- **LoRA**: Загрузка и выгрузка LoRAs на лету, обучение нового LoRA с использованием QLoRA.
- **Точные шаблоны инструкций для режима чата**: Включая Llama-2-chat, Alpaca, Vicuna, WizardLM, StableLM и многие другие.
- **Инференция на 4-бит, 8-бит и CPU**: Через библиотеку transformers.
- **Использование моделей llama.cpp с samplers transformers**: С использованием загрузчика llamacpp_HF.
- **Мультимодальные пайплайны**: Включая LLaVA и MiniGPT-4.
- **Пользовательские персонажи для чата**: Позволяет настроить внешний вид и поведение персонажей в чате. Ответ в зависимости от загатовленного характера, истории и описанной форме.
- **Очень эффективное текстовое потоковое вещание**: Обеспечивает быстрое и плавное взаимодействие с пользователем.
- **Вывод в формате Markdown с рендерингом LaTeX**: Например, для использования с GALACTICA.
- **API**: Включая конечные точки для потоковой передачи через веб-сокеты.

# gpt-engineer
Приложение позволяет локально анализировать код на соответствие требованиям, предлагать и вносить улучшения, писать тесты и вспомогательные модули.

https://github.com/AntonOsika/gpt-engineer

https://github.com/ivkhokhlov/rtk-gpt/assets/58159018/ae22143c-745e-4ec5-b589-af5b37979e42

#### Написание кода:
Позволяет генерировать и дорабатывать приложение с нуля, основываясь на базовых запросах. 
#### Исправление кода:
Дополнительные функции для работы с существующей кодовой базой
- `setup_sys_prompt(dbs)`: Устанавливает системный запрос, объединяя preprompt генерации и философский preprompt.
- `simple_gen(ai, dbs)`: Запускает AI на основном запросе и сохраняет результаты.
- `clarify(ai)`: Спрашивает у пользователя, хочет ли он что-то уточнить, и сохраняет результаты в рабочей области.
- `gen_spec(ai)`: Генерирует спецификацию из основного запроса + уточнений и сохраняет результаты в рабочей области.
- `respec(ai)`: Просит AI рассмотреть спецификацию новой функции и дать обратную связь по ней.
- `gen_unit_tests(ai)`: Генерирует модульные тесты на основе спецификации.
- `gen_clarified_code(ai)`: Генерирует код на основе основного запроса и уточнений.
- `gen_code(ai)`: Генерирует код на основе спецификации и модульных тестов.
- `gen_entrypoint(ai)`: Генерирует точку входа для сгенерированного кода.
- `use_feedback(ai)`: Использует обратную связь от пользователя для улучшения сгенерированного кода.
- `fix_code(ai)`: Исправляет любые ошибки в сгенерированном коде.
### Требования к железу
Модели разделяются по количеству параметров, например _7B - 7 миллиардов параметров, 13B - 13 миллиардов и так далее._
Требования к GPU зависят от количества параметров и размера используемой модели GPTQ. Если использовать ExLlama, которая на данный момент является наиболее производительной и эффективной библиотекой GPTQ, то:
- 7B требует карты объемом 6 ГБ
- 13B требует карту объемом 10 ГБ
- 30B/33B - карта объемом 24 ГБ или 2 x 12 ГБ.
- 65B/70B - карта 48 ГБ или 2 x 24 ГБ.
### Популярные модели на данный момент:
- Code LLama Python 65B - модификация Code Llama для Python, некоторых тестах обходит GPT-4
- Saiga2 - проект русскоязычного сообщества для ответов на русском
- Facebook Llama 2
- GPT4All
...

# stable-diffusion-webui
Генерация картинок по запросу с развитым API и веб-интерфейсом.
![image](https://github.com/ivkhokhlov/rtk-gpt/assets/58159018/9815a799-edaf-4a67-90b2-3af5487fb477)

https://github.com/ivkhokhlov/rtk-gpt/assets/58159018/8cc844e3-bb2b-4fcd-b1c8-21c9a8678493



# Основные фичи
- Браузерный интерфейс на основе библиотеки Gradio для Stable Diffusion.
- Поддержка API и специализированной модели inpainting от RunwayML.
- Оригинальные режимы txt2img и img2img.
- Функции Outpainting, Inpainting, Color Sketch и Prompt Matrix.
- Улучшение изображения с помощью Stable Diffusion Upscale.
- Возможность указать части текста, на которые модель должна обратить больше внимания.
- Loopback для многократной обработки img2img.
- X/Y/Z plot для создания 3D графиков изображений с разными параметрами.
- Текстовая инверсия и поддержка множественных вложений.
- Дополнительная вкладка с инструментами, такими как GFPGAN, RealESRGAN, ESRGAN и другие.
- Возможность изменения параметров шума и прерывания обработки в любое время.
- Поддержка обработки группы файлов с помощью img2img.
- Возможность загрузки различных VAE из экрана настроек.
- Поддержка Stable Diffusion 2.0 и Alt-Diffusion.
- Возможность изменения порядка элементов в пользовательском интерфейсе из экрана настроек.
- И многие другие функции, включая поддержку различных расширений и интеграций.


# Пример конфига
- **Видео**: 4090 x 2 - для запуска GPTQ моделей 65B/70B параметров
- **Память**: 1ТБ + SSD - для хранения моделей
- **БП**: 1500W - видеокарты до 500W + система
- **RAM**: 32GB - можно больше
- **CPU**: Ryzen 3900X - можно лучше
