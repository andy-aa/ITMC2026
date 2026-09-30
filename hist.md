# Рабочий контекст статьи ITMC 2026

## 1. Общая информация

Готовится полная научная статья для **ITMC 2026** (Springer conference proceedings) на английском языке.

Основная тема статьи:
**Computer Vision-Based Structural Analysis of Textile Medical Implants**

Цель статьи — описать и показать применение computer vision/image analysis для количественного структурного анализа и оценки качества текстильных медицинских имплантов.

Конференционные ограничения:

* английский язык;
* максимум 8 страниц A4;
* официальный Springer template;
* финальный вариант подаётся через ConfTool;
* статья должна быть оригинальной;
* необходимо соблюдать Springer proceedings requirements.

Официальные страницы:

* ITMC submission: https://itmc2026.ensait.fr/submission
* Springer conference proceedings: https://www.springernature.com/gp/authors/publish-a-book/step-by-step-conference-proceedings
* Springer technical instructions: https://itmc2026.ensait.fr/templates/SPLNPROC%20Technical%20Instructions.pdf

Дедлайн, который был установлен в ходе подготовки: **30 September 2026**.

---

# 2. Авторы

**Andrey Dyagilev¹* [0000-0001-6293-4819], Saskia Hesse¹, Pauline Riedl¹, Caroline Emonts¹ [0000-0001-6252-8351] and Thomas Gries¹ [0000-0002-2480-8333]**

Affiliation:

**Institut für Textiltechnik (ITA), RWTH Aachen University, Otto-Blumenthal-Straße 1, 52074 Aachen, Germany**

Corresponding email:

**[andrei.dziahileu@ita.rwth-aachen.de](mailto:andrei.dziahileu@ita.rwth-aachen.de)**

---

# 3. Главные научные объекты

Рассматриваются два разных типа текстильных медицинских имплантов:

1. **woven polyethylene terephthalate (PET) vascular grafts**
2. **braided Nitinol vascular stents**

Важно подчёркивать, что это две архитектурно разные структуры, поэтому для них используются разные architecture-specific structural descriptors.

Общая логика:

* microscopy image acquisition;
* preprocessing;
* structural feature extraction;
* quantitative/statistical analysis;
* quality assessment.

---

# 4. Общая научная идея статьи

Основная идея статьи:

**image acquisition → preprocessing → architecture-specific feature extraction → quantitative/statistical analysis → quality assessment**

Для woven structures анализируются:

* yarn arrangement;
* yarn spacing;
* yarn density;
* yarn geometry;
* weave repeat;
* individual yarn elements;
* local structural parameters;
* spatial variability.

Для braided structures анализируются:

* wire/braid lines;
* intersection points;
* braid cells;
* braiding angles;
* cell geometry;
* local structural parameters;
* spatial variability.

Полученные параметры позволяют:

* количественно характеризовать структуру;
* сравнивать разные ROI/regions;
* сравнивать разные specimens;
* выявлять локальные структурные отклонения;
* оценивать structural uniformity;
* поддерживать manufacturing quality assessment.

---

# 5. Стиль статьи

Пользователь предпочитает:

* detached, objective scientific style;
* писать «со стороны», а не в стиле “we developed / we propose”;
* избегать излишне рекламных формулировок;
* не делать слишком сильных утверждений;
* использовать осторожные формулировки: “can be used”, “may include”, “depending on image characteristics”, “where appropriate” — когда это действительно необходимо;
* текст должен быть компактным, поскольку ограничение статьи — 8 страниц;
* не превращать статью в учебник.

Особенно нежелательно:

* чрезмерно общие заявления;
* громкие слова без необходимости;
* слишком длинные объяснения базовой статистики;
* перечисление стандартных статистических тестов вроде “Shapiro–Wilk test, ANOVA” без реальной необходимости;
* элементарные формулы mean/SD/CV, если они не являются собственной существенной частью метода;
* называть простой histogram “distribution analysis” слишком громко;
* писать про “decision support”, если отдельной системы decision support фактически нет.

---

# 6. Текущая структура статьи

Сейчас согласована следующая структура:

## 1 Introduction

## 2 Materials and Methods

## 3 Results and Discussion

### 3.1 Woven PET Vascular Grafts

### 3.2 Braided Nitinol Vascular Stents

### 3.3 Structural Comparison and Quality Assessment

## 4 Conclusions

## Disclosure of Interests

## References

---

# 7. Почему выбран “Materials and Methods”

Изначально обсуждался вариант “Methods”, поскольку основной текст посвящён image analysis.

Однако было решено использовать:

**2 Materials and Methods**

потому что в разделе всё же кратко описываются реальные исследуемые материалы:

* woven PET vascular grafts;
* braided Nitinol vascular stents.

При этом Materials не должны превращаться в отдельный длинный раздел.

---

# 8. Текущий вариант Materials and Methods

Сейчас согласован следующий текст:

## 2 Materials and Methods

The study considers two structurally distinct types of textile medical implants: woven polyethylene terephthalate (PET) vascular grafts and braided Nitinol vascular stents. Their different architectures require architecture-specific procedures for the extraction and quantification of structural features from microscopy images.

The structural analysis and quality assessment are based on a sequential image-based workflow comprising image acquisition, preprocessing, structural feature extraction, quantitative analysis, and quality assessment (Fig. 1). The workflow provides a common basis for the analysis of both implant types while allowing the extraction of architecture-specific structural descriptors.

**Fig. 1.** Structural analysis and quality assessment pipeline.

The extracted geometric parameters are used to characterize local structural variability and to compare different image regions and implant specimens. Their statistical characteristics are subsequently considered for quality assessment and classification.

Важно: Fig. 1 должна стоять **не в конце всего раздела**, а сразу после абзаца, в котором она впервые упоминается.

---

# 9. Логика рисунков

Первоначально рассматривалась более подробная структура Methods с отдельными подразделами:

* Image Acquisition and Preprocessing;
* Structural Element Identification;
* Architecture-Specific Feature Extraction;
* Quantification and Statistical Analysis;
* Machine-Learning-Based Classification;
* Quality Assessment.

Однако для статьи на 8 страниц это оказалось слишком громоздко.

Было решено сделать Methods коротким, а детальные рисунки и конкретные процедуры перенести в Results and Discussion.

Главная логика:

**Methods отвечает на вопрос “как устроен общий workflow?”**

**Results and Discussion отвечает на вопрос “как этот workflow работает на конкретных имплантах и какие структурные параметры получаются?”**

---

# 10. Рисунок 1

Fig. 1 — общий workflow/pipeline.

Предполагаемая логика:

image acquisition → preprocessing → structural feature extraction → quantitative/statistical analysis → quality assessment

Fig. 1 остаётся в Materials and Methods.

Caption:

**Fig. 1. Structural analysis and quality assessment pipeline.**

---

# 11. Woven PET vascular grafts

Для woven PET grafts используется последовательный принцип анализа:

сначала определяются более крупные структурные единицы, затем внутри них — отдельные yarn elements.

Не стоит слишком сильно подчёркивать термин “hierarchical principle”, если в конкретном тексте это не нужно.

Основные этапы:

1. orientation correction;
2. ROI selection;
3. CNN-based pixel-wise classification;
4. weave repeat detection;
5. individual yarn identification;
6. extraction of geometric descriptors.

---

# 12. Fig. 2 — orientation correction

Fig. 2 показывает коррекцию ориентации изображения с использованием **2D FFT**.

Идея:

* текстильная структура имеет выраженную периодичность;
* 2D Fourier transform позволяет определить dominant orientation;
* изображение может быть повернуто в согласованную ориентацию перед дальнейшим анализом.

Это следует объяснять кратко и только в контексте конкретного анализа.

---

# 13. Fig. 3 — ROI selection

Fig. 3 показывает выбор **regions of interest (ROIs)**.

ROIs используются для:

* локального анализа;
* сравнения разных частей одного импланта;
* последующего анализа spatial variability.

Не следует делать из ROI selection слишком самостоятельный методический блок.

---

# 14. Fig. 4 — CNN pixel-wise classification

Для braided 3D structures microscopy images могут содержать:

* shadows;
* illumination variations;
* overlapping wires;
* visible backside wires;
* сложные фоновые области.

Поэтому простая thresholding-based segmentation может быть недостаточно надёжной.

Используется neural-network-based **pixel-wise classification**.

Важно использовать термин:

**pixel-wise classification**

или:

**class probability maps**

если CNN выдаёт class probabilities для каждого пикселя.

Не использовать автоматически термин **semantic segmentation**, если архитектура и ground truth задачи фактически этого не подтверждают.

CNN здесь лучше описывать как средство **structural element identification**, а не просто как preprocessing.

---

# 15. Woven structure: weave repeat

Для woven PET grafts:

Сначала определяются границы weave repeat.

Идея:

* периодическая структура создаёт периодические изменения image intensity;
* рассчитываются median intensity profiles вдоль x- и y-axes;
* характерные изменения профилей используются для определения spatial extent repeating unit.

После определения weave repeat его границы служат координатной системой для поиска отдельных yarn elements.

Возможный текст:

“The extraction of structural features follows a sequential procedure in which larger structural units are first identified and subsequently used as a reference for the identification of individual structural elements. For woven vascular grafts, the periodic arrangement of warp and weft yarns provides the basis for this procedure. First, the boundaries of the weave repeat are determined, and the individual yarn elements are then identified within the resulting structural unit.

The boundaries of the weave repeat can be identified from periodic variations in image intensity. Median intensity profiles are calculated along the x- and y-axes, and characteristic changes in the profiles are used to determine the spatial extent of the repeating unit. The detected boundaries therefore provide a coordinate reference for subsequent identification of individual yarn elements, as illustrated in Fig. 5.”

Caption:

**Fig. 5. Detection of weave repeat boundaries.**

---

# 16. Fig. 6 — individual yarn elements

Внутри identified weave repeat используются local intensity profiles для определения individual yarn elements и их boundaries.

Получаемые descriptors могут включать:

* yarn position;
* spacing;
* width;
* orientation;
* dimensions.

Процедура может применяться:

* к нескольким weave repeats;
* к разным image regions.

Это даёт набор local geometric descriptors для последующего quantitative/statistical analysis.

Возможный текст:

“Within the identified weave repeat, local intensity profiles can be used to detect individual yarn elements and their characteristic boundaries. The detected elements provide the basis for determining available geometric information, such as yarn position, spacing, width, orientation, and dimensions of the corresponding structural features. The procedure can be applied iteratively across multiple weave repeats and image regions, allowing a set of local geometric descriptors to be obtained from the analyzed structure. An example of individual yarn identification within a weave repeat is shown in Fig. 6.”

Caption:

**Fig. 6. Identification of individual yarn elements.**

---

# 17. Braided Nitinol stents

Для braided Nitinol stents есть важная особенность:

это 3D tubular geometry, а microscopy image является 2D projection of the stent surface.

Поэтому прямое измерение углов на projected image может давать distortion.

Используется **surface unwrapping** / **cylindrical surface unwrapping**.

Логика:

3D cylindrical/tubular surface → planar representation → wire trajectory analysis → intersection points → braid cells → braiding angle and cell geometry.

---

# 18. Surface unwrapping

Предпочтительный термин:

**surface unwrapping**

или более конкретно:

**cylindrical surface unwrapping**

После преобразования видимой поверхности стента в planar representation:

* уменьшается projection-related distortion;
* появляется более удобная coordinate system;
* wire trajectories можно анализировать более согласованно.

---

# 19. Fig. 7 — braid cells

После surface unwrapping:

* wire lines и intersection points определяются на основе pixel-wise classification;
* две wire families формируют braid;
* intersection points задают braid cells.

Для braid cells можно определять:

* cell area;
* characteristic dimensions;
* aspect ratio;
* shape-related descriptors;
* compactness — только если этот параметр действительно рассчитывается.

Не следует писать расплывчатое “cell angles”, если конкретная геометрическая величина не определена.

Возможный текст:

“For braided Nitinol stents, structural feature extraction has to account for the three-dimensional tubular geometry of the implant. A microscopy image represents a two-dimensional projection of the stent surface, and direct measurement of geometric parameters in the projected image can therefore introduce distortions, particularly for angular measurements. To obtain geometrically consistent measurements, the visible stent surface can be transformed into a planar representation using a surface-unwrapping procedure. This transformation provides a coordinate system in which the wire trajectories and their spatial relationships can be analyzed with reduced projection-related distortion.

Following surface unwrapping, the wire lines and their intersection points can be identified from the pixel-wise classification results. The two wire families forming the braid provide the basis for determining the braiding angle, which is an important geometric parameter of braided stents. In addition, the intersection points define individual braid cells, whose geometry can be characterized using parameters such as cell area, characteristic dimensions, aspect ratio, and shape-related descriptors such as compactness. The identified wire network and braid cells therefore provide complementary information on the local architecture of the stent.”

Caption:

**Fig. 7. Detection of braid cells in a Nitinol vascular stent: (a) stent surface and (b) enlarged view with detected braid lines and intersection points.**

---

# 20. Spatial/longitudinal comparison of braided stent

После определения geometric descriptors они могут сравниваться:

* между отдельными cells;
* между local image regions;
* вдоль longitudinal axis;
* между разными specimens.

Это позволяет выявлять:

* spatial changes in braiding angle;
* changes in braid-cell geometry;
* other structural variations.

Возможный текст:

“The resulting geometric descriptors can be determined for individual cells or local image regions and subsequently compared across the stent. Since the braided structure extends along the longitudinal axis of the stent, successive regions can be compared to identify spatial changes in braiding angle, braid-cell geometry, and other structural parameters. Such longitudinal analysis can provide information on the consistency of the braided structure and may support the assessment of process-related variations during stent manufacturing.”

---

# 21. Fig. 8 — braiding angle histograms

Fig. 8 показывает **измеренные braiding angles для того же Nitinol stent, который показан на Fig. 7**.

Угол измеряется отдельно для двух wire families:

* negative wire family;
* positive wire family.

Правильное описание:

“For the Nitinol stent shown in Fig. 7, the measured braiding angles were obtained separately for the two wire families. The corresponding histograms are shown in Fig. 8.”

Caption:

**Fig. 8. Histograms of the measured braiding angles for the Nitinol stent shown in Fig. 7: (a) negative and (b) positive wire families.**

Важно:

* не называть это просто “distribution analysis”;
* лучше говорить **histograms of the measured values**;
* фактические numerical results добавляются после получения конкретных данных.

---

# 22. Statistical analysis

Основная идея статистической части:

Не нужно превращать её в учебник статистики.

Не обязательно приводить:

* mean formula;
* SD formula;
* CV formula;
* Shapiro–Wilk;
* ANOVA и т. п., если они не являются действительно важными методами конкретного исследования.

Основной смысл:

полученные geometric descriptors статистически характеризуются для оценки:

* variability;
* spatial characteristics;
* local differences;
* differences between regions;
* differences between specimens.

Также можно сравнивать разные фрагменты одного объекта, чтобы оценивать manufacturing consistency.

Хорошая формулировка:

“The extracted geometric parameters are used to characterize local structural variability and to compare different image regions and implant specimens. Their statistical characteristics are subsequently considered for quality assessment and classification.”

---

# 23. Machine learning

В статье рассматриваются:

* Random Forest;
* Multilayer Perceptron (MLP);
* Convolutional Neural Network (CNN).

Но ML не должен искусственно доминировать в статье.

Особенно важно:

**CNN** используется в image-based structural element identification / pixel-wise classification.

Random Forest и MLP могут рассматриваться для automated classification based on extracted structural information/image features.

Если конкретные ML results не являются центральной частью Results, не следует делать ML главным итогом статьи.

В частности, в Conclusions **не нужно заканчивать статью машинным обучением**.

---

# 24. Introduction — утверждённый текущий текст

Текущий approved Introduction:

Textile-based materials are widely used in medical implants because their fibrous architectures can be tailored to provide specific mechanical and functional properties. Weaving and braiding technologies are employed in vascular grafts and stent structures, where parameters such as porosity, compliance, and structural arrangement can influence implant performance [1, 2]. The resulting textile architectures are therefore not only manufacturing features but also important characteristics for the functional assessment and quality control of medical implants.

Woven and braided architectures are particularly relevant for vascular implants. Woven grafts consist of interlaced warp and weft yarns, with structural parameters such as yarn density, spacing, and pore geometry affecting permeability and related functional properties [3]. Braided implants, in contrast, consist of interlaced filaments or wires, where parameters such as braiding angle, filament diameter, and strand configuration influence porosity and mechanical behaviour [4, 5]. Despite these architectural differences, both types of implants depend on the precise spatial organization of their constituent elements. Local variations in filament spacing, orientation, pore geometry, and density may occur during manufacturing and can result in structural variability.

Microscopy-based image analysis provides a suitable means of quantitatively characterizing such structural features. For woven structures, relevant descriptors include yarn density, spacing, orientation, and pore geometry, whereas braided structures can be characterized using parameters such as braiding angle, filament diameter, and strand configuration [4]. Previous studies have demonstrated the automated analysis of textile structures using image-processing techniques, including the measurement of yarn spacing and orientation [6], as well as image-based characterization of porosity-related parameters in woven fabrics [7]. These studies demonstrate the feasibility of extracting quantitative structural information directly from images.

Computer vision and machine learning have further expanded the possibilities for automated textile analysis. Image-processing methods have been used for the recognition and measurement of woven structural parameters, including fabric density and weave patterns [8, 9]. Convolutional neural networks have also been applied to the recognition of textile structures directly from images [10], while neural approaches have been investigated for extracting geometric yarn information [11]. More recent work has demonstrated the combination of computer vision and deep learning for quantitative yarn quality analysis [12]. These developments indicate that automated image-based methods can provide objective and reproducible information for structural characterization and quality assessment.

However, existing approaches mainly focus on individual structural parameters or specific recognition tasks, with particular emphasis on conventional woven textile structures [6, 8]. Less attention has been given to frameworks that combine architecture-specific structural feature extraction with statistical characterization of spatial variability and subsequent automated quality classification. This is particularly relevant for textile medical implants, where structurally different architectures require different quantitative descriptors while sharing the need for objective and reproducible assessment. In addition, manufacturing quality cannot be adequately described by nominal parameter values alone, since local deviations and spatial variability may provide important information about structural uniformity.

To address this gap, this study develops and evaluates a computer vision-based framework for the automated structural analysis and quality assessment of textile medical implants. The framework combines image-based extraction of architecture-specific structural descriptors with statistical analysis of their distributions and spatial variability. Two structurally distinct implant types are considered: woven polyethylene terephthalate vascular grafts and braided Nitinol vascular stents. For the woven grafts, the analysis focuses on parameters describing yarn arrangement and geometry, whereas for the braided stents, parameters such as braiding angle and cell geometry are extracted. In addition, Random Forest, Multilayer Perceptron, and Convolutional Neural Network models are investigated for automated structural quality classification. The overall objective is to establish a quantitative and reproducible basis for structural quality assessment that can support data-driven quality control and process monitoring in the manufacturing of textile medical implants.

Замечание на будущее: последняя часть Introduction использует “this study develops and evaluates...” — если будем дополнительно унифицировать detached style, можно позже заменить на более нейтральную формулировку.

---

# 25. Abstract — текущий вариант

Abstract:

Textile medical implants exhibit complex fibrous architectures whose structural characteristics can directly affect their functional performance and manufacturing quality. Reliable and reproducible characterization of these structures is therefore essential for quality assessment and process monitoring. This study presents a computer vision-based framework for the automated structural analysis and statistical quality assessment of textile medical implants using microscopy images. The proposed approach was applied to two structurally distinct implant types: woven polyethylene terephthalate vascular grafts and braided Nitinol vascular stents. Image-processing and machine-learning methods were used to identify architecture-specific structural features. For the woven grafts, the framework quantifies parameters describing yarn arrangement and geometry, while for the braided stents, parameters such as braiding angle and cell geometry are extracted. The resulting structural descriptors are statistically evaluated to characterize their distributions and spatial variability and to identify deviations from the expected structural characteristics. In addition, machine-learning models are investigated for automated classification based on the extracted structural information and image data. The results demonstrate the potential of the proposed framework to provide objective and reproducible quantitative information on textile implant architectures. By combining automated feature extraction, statistical characterization, and machine-learning-based analysis, the approach provides a basis for structural quality assessment and can support data-driven quality and process-control decisions in the manufacturing of textile medical implants.

Замечание: пользователь считает некоторые “proposed approach/framework” formulations слишком прямыми; Abstract при необходимости следует сделать более detached.

---

# 26. Keywords

computer vision, textile medical implants, structural quality assessment, image analysis, machine learning, statistical analysis

---

# 27. Conclusions — текущий согласованный вариант

## 4 Conclusions

A computer vision-based approach for the structural analysis and quality assessment of textile medical implants was considered for two structurally distinct implant architectures: woven polyethylene terephthalate (PET) vascular grafts and braided Nitinol vascular stents. The analysis demonstrates that microscopy images can be used to extract architecture-specific geometric descriptors that characterize the spatial organization of the corresponding textile structures.

For woven PET vascular grafts, the analysis enables the identification and quantification of structural features related to yarn arrangement and geometry. For braided Nitinol vascular stents, the structural analysis includes the characterization of wire trajectories, braiding angles, and braid-cell geometry. The extracted parameters allow local structural variations to be quantified and compared between different regions and implant specimens.

Statistical evaluation of the extracted geometric parameters provides information on their variability and spatial characteristics. This enables deviations in structural characteristics to be identified and provides a basis for assessing structural uniformity and manufacturing quality. The combination of automated image analysis and quantitative structural characterization therefore supports an objective and reproducible assessment of textile medical implant architectures.

Важно: **не заканчивать Conclusions машинным обучением**, если ML не является центральным итогом статьи.

---

# 28. Disclosure of Interests

Текущий вариант:

**Disclosure of Interests. The authors have no competing interests to declare that are relevant to the content of this article.**

Если Springer template требует отдельный heading, использовать:

## Disclosure of Interests

The authors have no competing interests to declare that are relevant to the content of this article.

---

# 29. References

Текущий список 1–12:

1. Singh, C., Wong, C.S., Wang, X.: Medical textiles as vascular implants and their success to mimic natural arteries. Journal of Functional Biomaterials. 6, 500–525 (2015). DOI 10.3390/jfb6030500

2. Bakare, A., Mohanadas, H.P., Tucker, N., Ahmed, W., Manikandan, A., Faudzi, A.A.M., Mohamaddan, S., Jaganathan, S.K.: Advancements in textile techniques for cardiovascular tissue replacement and repair. APL Bioengineering. 8, (2024). DOI 10.1063/5.0231856

3. Guan, G., Yu, C., Fang, X., Guidoin, R., King, M.W., Wang, H., Wang, L.: Exploration into practical significance of integral water permeability of textile vascular grafts. Journal of Applied Biomaterials & Functional Materials. 19, (2021). DOI 10.1177/22808000211014007

4. Rebelo, R., Vila, N., Fangueiro, R., Carvalho, S., Rana, S.: Influence of design parameters on the mechanical behavior and porosity of braided fibrous stents. Materials & Design. 86, 237–247 (2015). DOI 10.1016/j.matdes.2015.07.051

5. Zheng, Q., Mozafari, H., Li, Z., Gu, L., An, M., Han, X., You, Z.: Mechanical characterization of braided self-expanding stents: Impact of design parameters. Journal of Mechanics in Medicine and Biology. 19, 1950038 (2019). DOI 10.1142/S0219519419500386

6. Kang, T.J., Choi, S.H., Kim, S.M., Oh, K.W.: Automatic structure analysis and objective evaluation of woven fabric using image analysis. Textile Research Journal. 71, 261–270 (2001). DOI 10.1177/004051750107100312

7. Zupin, Ž., Štampfl, V., Kočevar, T.N., Gabrijelčič Tomc, H.: Comparison of measured and calculated porosity parameters of woven fabrics to results obtained with image analysis. Materials. 17, 783 (2024). DOI 10.3390/ma17040783

8. Meng, S., Pan, R., Gao, W., Yan, B., Peng, Y.: Automatic recognition of woven fabric structural parameters: A review. Artificial Intelligence Review. 55, 6345–6387 (2022). DOI 10.1007/s10462-022-10156-x

9. Xiang, J., Pan, R.: Automatic recognition of density and weave pattern of yarn-dyed fabric. AUTEX Research Journal. 23, 504–513 (2022). DOI 10.2478/aut-2022-0025

10. Xiao, Z., Liu, X., Wu, J., Geng, L., Sun, Y., Zhang, F., Tong, J.: Knitted fabric structure recognition based on deep learning. The Journal of The Textile Institute. 109, 1217–1223 (2018). DOI 10.1080/00405000.2017.1422309

11. Trunz, E., Klein, J., Müller, J., Bode, L., Sarlette, R., Weinmann, M., Klein, R.: Neural inverse procedural modeling of knitting yarns from images. Computers & Graphics. 118, 161–172 (2024). DOI 10.1016/j.cag.2023.12.013

12. Pereira, F., Lopes, H., Pinto, L., Soares, F., Vasconcelos, R., Machado, J., Carvalho, V.: Yarn quality analysis by using computer vision and deep learning techniques. Textile Research Journal. 96, 240–265 (2025). DOI 10.1177/00405175251331205

Metadata for references [2] and [3] should be verified before final submission.

---

# 30. Важные терминологические решения

Использовать:

* **woven PET vascular grafts**
* **braided Nitinol vascular stents**
* **structural descriptors**
* **geometric parameters**
* **architecture-specific structural features**
* **pixel-wise classification**
* **class probability maps**
* **surface unwrapping**
* **cylindrical surface unwrapping**
* **braid cells**
* **intersection points**
* **wire families**
* **braiding angle**
* **local structural variability**
* **spatial variability**
* **structural uniformity**
* **manufacturing quality**

Осторожно использовать:

* semantic segmentation;
* hierarchical analysis;
* distribution analysis;
* decision support;
* compactness — только если реально рассчитывается.

---

# 31. Логика размещения рисунков

Предлагаемое размещение:

### Section 2 Materials and Methods

**Fig. 1** — overall structural analysis and quality assessment pipeline.

### Section 3.1 Woven PET Vascular Grafts

**Fig. 2** — orientation correction using 2D FFT.
**Fig. 3** — ROI selection.
**Fig. 4** — CNN architecture / pixel-wise classification.
**Fig. 5** — weave repeat boundaries.
**Fig. 6** — individual yarn elements.

### Section 3.2 Braided Nitinol Vascular Stents

**Fig. 7** — braid-cell detection, wire lines and intersection points.
**Fig. 8** — histograms of measured braiding angles for the same Nitinol stent shown in Fig. 7, separately for negative and positive wire families.

### Section 3.3 Structural Comparison and Quality Assessment

Здесь желательно уже использовать:

* tables;
* quantitative comparisons;
* statistical summaries;
* quality-related comparisons;
* ML classification results, если они действительно есть и достаточно значимы.

---

# 32. Главная логика Results and Discussion

Не делать Results как повтор Methods.

Например:

### 3.1 Woven PET Vascular Grafts

Сначала кратко вводится конкретный PET graft и результат анализа.

Далее:

* orientation correction;
* ROI;
* CNN/pixel classification;
* weave repeat;
* yarn elements;
* quantitative descriptors.

Каждый рисунок показывает **реальный пример применения метода**, а не просто абстрактную схему.

### 3.2 Braided Nitinol Vascular Stents

* 3D tubular geometry;
* surface unwrapping;
* wire identification;
* braid cells;
* braiding angles;
* Fig. 7;
* Fig. 8;
* spatial variation.

### 3.3 Structural Comparison and Quality Assessment

* сравнение regions;
* сравнение specimens;
* variability;
* deviations;
* quality assessment;
* ML classification, если есть полноценные результаты.

---

# 33. Что НЕ надо делать в следующей версии

Не возвращаться автоматически к:

* длинному “2.1 Image Acquisition and Preprocessing”;
* “2.2 Structural Element Identification”;
* длинному списку statistical tests;
* отдельному “Decision Support”;
* длинным формулам для elementary statistics;
* чрезмерному описанию CNN architecture, если это не основной результат;
* выводу, заканчивающемуся machine learning;
* слишком общим словам вроде “distribution analysis” для обычных histograms.

---

# 34. Основной принцип всей статьи

Статья должна читаться как единая цепочка:

**Textile implant architecture**
→ **microscopy image**
→ **image processing**
→ **architecture-specific structural element identification**
→ **geometric descriptors**
→ **local/spatial variability**
→ **statistical characterization**
→ **structural quality assessment**

При этом woven и braided structures имеют разные конкретные алгоритмы, но объединены одной общей логикой количественного image-based structural assessment.

Главный результат статьи — не сам CNN и не отдельный алгоритм, а возможность **объективно и воспроизводимо количественно характеризовать структуру текстильных медицинских имплантов и использовать полученные параметры для оценки структурной однородности и производственного качества.**
