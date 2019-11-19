# Select features for same value
```bash
layer = QgsProject.instance().mapLayer('[% @layer_id %]')
layer.selectByExpression('"land_type"=\'[%land_type%]\'')

```
# Filter Multiple Values
```bash
example:
"Field Name" IN ('Value_1', 'Value_2', 'Value_3',...,'Value_N')

"ELEV" IN (500, 700, 1000, 1200, 1500, 1700, 2000, 2300, 2500)

```
