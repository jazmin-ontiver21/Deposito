# TODO: Fix Descartable Issues

## Step 1: Fix models.py - fecha_dispensa field
- [x] Change `fecha_dispensa = models.DateField()or None` → `models.DateField(null=True, blank=True)`

## Step 2: Add buscar_descartable_lote view in views.py
- [x] Add `buscar_descartable_lote()` function filtering by `lote__icontains`

## Step 3: Update reporte_diario() to include RemitoDescartable
- [x] Import `RemitoDescartable` from remito.models
- [x] Query remito-based descartable dispensations for today
- [x] Combine with existing Dispensa data

## Step 4: Update descartable_mas_dispensados() to include RemitoDescartable
- [x] Aggregate RemitoDescartable from last 7 days
- [x] Combine with existing Dispensa aggregates

## Step 5: Add URL for buscar_descartable_lote in urls.py
- [x] Add path for `buscar_descartable_lote`

## Step 6: Fix lista_descartable.html - lote search form action
- [x] Change second form's action from `buscar_descartable` to `buscar_descartable_lote`

## Step 7: Run migrations
- [x] Migration `0003_alter_descartable_fecha_dispensa.py` already existed
- [x] `python manage.py migrate` applied successfully

