анализируй требования для буликации полных статей 

https://itmc2026.ensait.fr/submission

https://www.springernature.com/gp/authors/publish-a-book/step-by-step-conference-proceedings



# CONTEXT FOR CONTINUING WORK ON ITMC 2026 PAPER

## 1. Общая задача

Я готовлю полную научную статью для конференции **ITMC 2026** и последующей публикации в **Springer conference proceedings**.

Работа посвящена computer vision / image analysis для структурного анализа и оценки качества текстильных медицинских имплантов.

Я вручную переношу готовый текст в официальный Springer template. Поэтому при дальнейшей работе нужно давать мне **готовый английский текст для вставки в шаблон**, а не Pandoc Markdown с `@citation_keys`.

---

## 2. Конференция и формат

ITMC 2026:
https://itmc2026.ensait.fr/submission

Springer Nature conference proceedings:
https://www.springernature.com/gp/authors/publish-a-book/step-by-step-conference-proceedings

Изученные требования:

* full paper на английском языке;
* максимум 8 страниц A4;
* используется официальный template;
* submission через ConfTool;
* авторский список и порядок авторов должны быть окончательными;
* работа должна быть оригинальной и не находиться одновременно на рассмотрении в другом месте;
* для публикации используются правила Springer conference proceedings.

Я вручную переношу материал в Springer template.

---

## 3. Название статьи

Основной выбранный вариант:

**Computer Vision-Based Structural Analysis of Textile Medical Implants**

Рассматривался более длинный вариант:

**Computer Vision-Based Structural Analysis and Statistical Quality Assessment of Textile Medical Implants**

Но было решено, что короткий вариант лучше, поскольку структурный анализ является основной частью работы, а quality assessment — его последующим применением.

---

## 4. Авторы

Полный список:

**Andrey Dyagilev¹* [0000-0001-6293-4819], Saskia Hesse¹, Pauline Riedl¹, Caroline Emonts¹ [0000-0001-6252-8351] and Thomas Gries¹ [0000-0002-2480-8333]**

Ранее обсуждался shortened/running title автора:

**A. Dyagilev et al.**

или полный вариант:

**A. Dyagilev, S. Hesse, P. Riedl, C. Emonts and T. Gries**

ORCID не нужно помещать в running head.

---

## 5. Основная идея статьи

Статья предлагает computer vision-based framework для автоматизированного анализа структуры и оценки качества textile medical implants.

Рассматриваются два различных типа имплантов:

1. **Woven polyethylene terephthalate (PET) vascular grafts**
2. **Braided Nitinol vascular stents**

Главная идея:

**image acquisition → preprocessing → feature extraction → statistical analysis → quality assessment / decision support**

Для разных архитектур используются разные структурные признаки.

### Для woven grafts:

* yarn arrangement;
* yarn spacing;
* yarn density;
* yarn geometry;
* weave repeat;
* individual yarn elements;
* local structural parameters;
* spatial variability.

### Для braided Nitinol stents:

* braid lines / wire lines;
* intersection points;
* braid cells;
* braiding angles;
* cell geometry;
* local structural parameters.

После извлечения параметров они могут:

* анализироваться статистически;
* сравниваться между различными regions of interest;
* использоваться для quality assessment;
* использоваться как признаки для ML classification.

---

## 6. Введение — утверждённая логика

Introduction построено в следующем порядке:

### Paragraph 1

Значение textile-based materials для medical implants; woven и braided technologies; structural parameters влияют на функциональные свойства.

### Paragraph 2

Различия между woven и braided architectures и необходимость количественного анализа spatial organization.

### Paragraph 3

Microscopy-based image analysis как способ количественного определения structural features.

### Paragraph 4

Computer vision и machine learning для автоматизированного textile analysis.

### Paragraph 5

Research gap:

* существующие работы часто сосредоточены на отдельных параметрах;
* много внимания уделено conventional woven textiles;
* меньше работ объединяют architecture-specific feature extraction, statistical characterization of spatial variability и automated quality classification;
* nominal parameter values сами по себе недостаточны для описания manufacturing quality.

### Final paragraph

Цель данной работы — разработать и оценить computer vision-based framework для automated structural analysis and quality assessment of textile medical implants.

---

## 7. Введение — текущая версия

Textile-based materials are widely used in medical implants because their fibrous architectures can be tailored to provide specific mechanical and functional properties. Weaving and braiding technologies are employed in vascular grafts and stent structures, where parameters such as porosity, compliance, and structural arrangement can influence implant performance [1, 2]. The resulting textile architectures are therefore not only manufacturing features but also important characteristics for the functional assessment and quality control of medical implants.

Woven and braided architectures are particularly relevant for vascular implants. Woven grafts consist of interlaced warp and weft yarns, with structural parameters such as yarn density, spacing, and pore geometry affecting permeability and related functional properties [3]. Braided implants, in contrast, consist of interlaced filaments or wires, where parameters such as braiding angle, filament diameter, and strand configuration influence porosity and mechanical behaviour [4, 5]. Despite these architectural differences, both types of implants depend on the precise spatial organization of their constituent elements. Local variations in filament spacing, orientation, pore geometry, and density may occur during manufacturing and can result in structural variability.

Microscopy-based image analysis provides a suitable means of quantitatively characterizing such structural features. For woven structures, relevant descriptors include yarn density, spacing, orientation, and pore geometry, whereas braided structures can be characterized using parameters such as braiding angle, filament diameter, and strand configuration [4]. Previous studies have demonstrated the automated analysis of textile structures using image-processing techniques, including the measurement of yarn spacing and orientation [6], as well as image-based characterization of porosity-related parameters in woven fabrics [7]. These studies demonstrate the feasibility of extracting quantitative structural information directly from images.

Computer vision and machine learning have further expanded the possibilities for automated textile analysis. Image-processing methods have been used for the recognition and measurement of woven structural parameters, including fabric density and weave patterns [8, 9]. Convolutional neural networks have also been applied to the recognition of textile structures directly from images [10], while neural approaches have been investigated for extracting geometric yarn information [11]. More recent work has demonstrated the combination of computer vision and deep learning for quantitative yarn quality analysis [12]. These developments indicate that automated image-based methods can provide objective and reproducible information for structural characterization and quality assessment.

However, existing approaches mainly focus on individual structural parameters or specific recognition tasks, with particular emphasis on conventional woven textile structures [6, 8]. Less attention has been given to frameworks that combine architecture-specific structural feature extraction with statistical characterization of spatial variability and subsequent automated quality classification. This is particularly relevant for textile medical implants, where structurally different architectures require different quantitative descriptors while sharing the need for objective and reproducible assessment. In addition, manufacturing quality cannot be adequately described by nominal parameter values alone, since local deviations and spatial variability may provide important information about structural uniformity.

To address this gap, this study develops and evaluates a computer vision-based framework for the automated structural analysis and quality assessment of textile medical implants. The framework combines image-based extraction of architecture-specific structural descriptors with statistical analysis of their distributions and spatial variability. Two structurally distinct implant types are considered: woven polyethylene terephthalate vascular grafts and braided Nitinol vascular stents. For the woven grafts, the analysis focuses on parameters describing yarn arrangement and geometry, whereas for the braided stents, parameters such as braiding angle and cell geometry are extracted. In addition, Random Forest, Multilayer Perceptron, and Convolutional Neural Network models are investigated for automated structural quality classification. The overall objective is to establish a quantitative and reproducible basis for structural quality assessment that can support data-driven quality control and process monitoring in the manufacturing of textile medical implants.

---

## 8. References и порядок цитирования

Список из 12 references:

1. Singh, C., Wong, C.S., Wang, X.: Medical textiles as vascular implants and their success to mimic natural arteries. Journal of Functional Biomaterials. 6, 500–525 (2015). https://doi.org/10.3390/jfb6030500

2. Bakare, A., Mohanadas, H.P., Tucker, N., Ahmed, W., Manikandan, A., Faudzi, A.A.M., Mohamaddan, S., Jaganathan, S.K.: Advancements in textile techniques for cardiovascular tissue replacement and repair. APL Bioengineering. 8, (2024). https://doi.org/10.1063/5.0231856

3. Guan, G., Yu, C., Fang, X., Guidoin, R., King, M.W., Wang, H., Wang, L.: Exploration into practical significance of integral water permeability of textile vascular grafts. Journal of Applied Biomaterials & Functional Materials. 19, (2021). https://doi.org/10.1177/22808000211014007

4. Rebelo, R., Vila, N., Fangueiro, R., Carvalho, S., Rana, S.: Influence of design parameters on the mechanical behavior and porosity of braided fibrous stents. Materials & Design. 86, 237–247 (2015). https://doi.org/10.1016/j.matdes.2015.07.051

5. Zheng, Q., Mozafari, H., Li, Z., Gu, L., An, M., Han, X., You, Z.: Mechanical characterization of braided self-expanding stents: Impact of design parameters. Journal of Mechanics in Medicine and Biology. 19, 1950038 (2019). https://doi.org/10.1142/S0219519419500386

6. Kang, T.J., Choi, S.H., Kim, S.M., Oh, K.W.: Automatic structure analysis and objective evaluation of woven fabric using image analysis. Textile Research Journal. 71, 261–270 (2001). https://doi.org/10.1177/004051750107100312

7. Zupin, Ž., Štampfl, V., Kočevar, T.N., Gabrijelčič Tomc, H.: Comparison of measured and calculated porosity parameters of woven fabrics to results obtained with image analysis. Materials. 17, 783 (2024). https://doi.org/10.3390/ma17040783

8. Meng, S., Pan, R., Gao, W., Yan, B., Peng, Y.: Automatic recognition of woven fabric structural parameters: A review. Artificial Intelligence Review. 55, 6345–6387 (2022). https://doi.org/10.1007/s10462-022-10156-x

9. Xiang, J., Pan, R.: Automatic recognition of density and weave pattern of yarn-dyed fabric. AUTEX Research Journal. 23, 504–513 (2022). https://doi.org/10.2478/aut-2022-0025

10. Xiao, Z., Liu, X., Wu, J., Geng, L., Sun, Y., Zhang, F., Tong, J.: Knitted fabric structure recognition based on deep learning. The Journal of The Textile Institute. 109, 1217–1223 (2018). https://doi.org/10.1080/00405000.2017.1422309

11. Trunz, E., Klein, J., Müller, J., Bode, L., Sarlette, R., Weinmann, M., Klein, R.: Neural inverse procedural modeling of knitting yarns from images. Computers & Graphics. 118, 161–172 (2024). https://doi.org/10.1016/j.cag.2023.12.013

12. Pereira, F., Lopes, H., Pinto, L., Soares, F., Vasconcelos, R., Machado, J., Carvalho, V.: Yarn quality analysis by using computer vision and deep learning techniques. Textile Research Journal. 96, 240–265 (2025). https://doi.org/10.1177/00405175251331205

Важно: metadata для references [2] и [3] ранее были отмечены как потенциально неполные. Если будем финально проверять bibliography, нужно проверить их DOI и полные bibliographic details.

---

## 9. Нумерация citations в Introduction

При ручном переносе в Springer template используются готовые числовые ссылки:

[1, 2]
[3]
[4, 5]
[6, 7]
[8, 9]
[10, 11]
[12]
[6, 8]

Не использовать в ручном Springer template Pandoc keys вроде `@Kang2001`.

Порядок references уже соответствует порядку первого появления в Introduction.

---

# 10. Figures — уже согласованные captions

## Figure 1 — overall pipeline

На схеме:

Image Acquisition
→ Preprocessing
→ Feature Extraction
→ Statistical Analysis
→ Quality Assessment & Decision Support

Выбран caption:

**Fig. 1. Structural analysis and quality assessment pipeline.**

Не использовать слово "Proposed".

---

## Figure 2 — CNN pixel-wise classification

На рисунке:

* input image;
* CNN architecture;
* layers and connections;
* output pseudo-image;
* probability maps for different classes;
* задача pixel-wise classification для выделения нужной части импланта.

Рекомендуемый caption:

**Fig. 2. CNN architecture for pixel-wise classification of implant structures.**

Важно: если output именно probability maps, а не обычная segmentation mask, лучше сохранять термин **pixel-wise classification**.

---

## Figure 3 — FFT orientation correction

(a) fragment of vascular graft surface under microscope.

(b) 2D FFT spectrum with intensity peaks. Lines through the peaks and coordinate axes define the correction angle. В данном случае исходное изображение необходимо повернуть на 2°.

Выбранный caption:

**Fig. 3. Orientation correction of a vascular graft image using 2D FFT analysis: (a) microscopic image and (b) 2D Fourier spectrum.**

Можно не писать 2° в caption, если 2° уже непосредственно показано на рисунке.

---

## Figure 4 — weave repeat detection

Центральное изображение — woven graft surface.

Сверху и справа — plots of median gray-level intensity along x- and y-axes.

Минимумы intensity profiles используются для определения границ weave repeats. Границы показаны на центральном изображении.

Выбранный caption:

**Fig. 4. Detection of weave repeat boundaries from median intensity profiles along the x- and y-axes.**

---

## Figure 5 — individual yarn elements

Выделен один weave repeat из предыдущего рисунка.

Сверху снова показан intensity profile.

По нему определяются отдельные элементарные элементы yarn.

Выбранный caption:

**Fig. 5. Identification of individual yarn elements using intensity profiles within the weave repeat.**

Важно:
использовать **yarn elements**, а не "chemical elements". Здесь речь об отдельных элементах/участках пряжи, а не о химических элементах.

---

## Figure 6 — regions of interest

На изображении woven graft surface показаны четыре прямоугольных региона разной формы, цвета и размера.

Смысл:

* выбирается region of interest (ROI);
* внутри ROI измеряются geometric parameters of elementary yarn elements;
* собранные параметры могут анализироваться самостоятельно;
* регионы можно сравнивать между собой.

Выбранный caption:

**Fig. 6. Selection of regions of interest for local structural analysis.**

Это предпочтительнее длинного описания в caption; подробности можно дать в основном тексте.

---

## Figure 7 — braided Nitinol stent / braid cells

(a) braided Nitinol vascular stent.

(b) enlarged fragment of braid structure.

На увеличенном фрагменте:

* detected braid/wire lines;
* intersection points;
* на их основе выделяются braid cells.

Обсуждалась терминология.

Для braided stents более уместно говорить:

* **braid cells**
* **cell geometry**
* **intersection points**
* **braid lines / wire lines**

Если на рисунке именно выделены ячейки, термин **braid cells** предпочтительнее, чем просто "detected braid lines".

Рекомендуемый caption:

**Fig. 7. Detection of braid cells in a Nitinol vascular stent: (a) stent surface and (b) enlarged view with detected braid cells.**

Если на изображении визуально явно показаны именно lines and intersection points, можно использовать:

**Fig. 7. Braid structure analysis of a Nitinol vascular stent: (a) stent surface and (b) enlarged view with detected braid lines and intersection points.**

---

## Figure 8 — braiding angle histograms

Две гистограммы:
(a) negative braiding angles;
(b) positive braiding angles.

Это две системы проволок / wire directions в braided stent.

Терминологически обсуждалось:

* two wire families;
* two sets of wires;
* two groups of wires.

Для научной статьи предпочтительно **two wire families**, если речь именно о двух системах проволок с противоположными направлениями.

Рекомендуемый caption:

**Fig. 8. Distribution of braiding angles for the two wire families: (a) negative and (b) positive angles.**

Возможный более простой вариант:

**Fig. 8. Distribution of braiding angles for the two sets of wires: (a) negative and (b) positive angles.**

Терминологическая логика:
**two wire families → opposite winding directions → signed braiding angles**

Для Nitinol stent лучше использовать **wire**, а не **filament**, поскольку это металлическая проволока.

---

# 11. Терминология, которую желательно сохранять последовательно

### Woven graft:

* woven structure
* woven graft
* yarn
* yarn element
* yarn spacing
* yarn density
* weave repeat
* weave repeat boundary
* region of interest (ROI)
* geometric parameters
* gray-level intensity
* intensity profile
* spatial variability

### Braided stent:

* braided stent
* Nitinol wire
* wire family / two wire families
* braid line
* intersection point
* braid cell
* cell geometry
* braiding angle
* positive/negative braiding angle
* opposite winding directions

### Computer vision / ML:

* image acquisition
* preprocessing
* feature extraction
* statistical analysis
* quality assessment
* decision support
* pixel-wise classification
* CNN
* Random Forest
* Multilayer Perceptron (MLP)

---

# 12. Важное различие в терминологии CNN

Если CNN выдаёт для каждого пикселя вероятности принадлежности к разным классам, это следует описывать как:

**pixel-wise classification**

или, если архитектура и задача действительно соответствуют segmentation:

**semantic segmentation**

Но если в статье принципиально говорится именно о классификации каждого пикселя и показываются class probability maps, пока предпочтительно использовать:

**pixel-wise classification**

Не называть автоматически результат "segmentation mask", если выходом являются probability maps.

---

# 13. Стиль captions

Для всех рисунков желательно придерживаться одного стиля Springer:

**Fig. X. Short descriptive caption.**

Если есть панели:

**Fig. X. Description: (a) ... and (b) ...**

Captions должны быть:

* короткими;
* технически точными;
* без лишнего объяснения алгоритма;
* без повторения длинного текста из Methods;
* на английском;
* без слова "Proposed", если оно не нужно.

---

# 14. Что делать дальше

При продолжении работы желательно идти последовательно по paper:

1. Title
2. Authors
3. Abstract
4. Keywords
5. Introduction
6. Fig. 1 — pipeline
7. Methods
8. Woven graft analysis
9. Braided stent analysis
10. CNN / ML methods
11. Statistical analysis
12. Results
13. Quality assessment
14. Conclusion
15. References

Основная задача — привести весь paper к единому Springer conference style, сохранив научный смысл и не раздувая текст, так как ограничение — 8 страниц.

Если я прошу "caption", нужно давать короткую готовую английскую подпись для вставки в Springer template.

Если я присылаю русский текст/описание рисунка, нужно сначала понять научный смысл, а затем предложить естественную академическую формулировку на английском, а не переводить буквально.

Если я прошу проверить терминологию, желательно сверяться с научной литературой, особенно для терминов braided stents, woven grafts, braid cells, braiding angles и image-based textile analysis.

---

# 15. Текущий принцип работы

Я хочу, чтобы статья звучала как нормальная международная научная публикация, а не как буквальный перевод с русского.

Предпочтение:

* concise academic English;
* точная техническая терминология;
* короткие captions;
* минимизация повторов;
* ясная связь между method → extracted parameters → statistical analysis → quality assessment;
* не перегружать captions деталями, которые лучше объяснить в Methods.

Главная научная линия статьи:

**computer vision → architecture-specific structural feature extraction → statistical characterization → quality assessment / classification**

для двух разных textile medical implant architectures:
**woven PET vascular grafts** и **braided Nitinol vascular stents**.
