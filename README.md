Код решения 25 места (серебро) (приведена только моя часть решения, итоговое решение - ансамбль решения 5 участников)

Модель: efficientnet-b4
Аугментации: VerticalFlip(p=0.5), HorizontalFlip(p=0.5), RandomRotate90(p=0.5), 
Cutout(max_h_size=50,max_w_size=50), CoarseDropout(max_height=50, max_width=50)], p=0.5), 
Normalize(mean=(0.485,0.456,0.406),std=(0.229,0.224,0.225),max_pixel_value=255.0)

Лосс: CrossEntropyLoss

Оптимизатор: AdamW

Scheduler: CosineAnnealingLR

Метрика: WAUC

TTA: D4

n_folds = 5

Как запустить: выполнить все ячейки в ноутбуке my_ideas_public.ipynb

Время тренировки: примерно 3-е суток на 1 x TeslaV100.