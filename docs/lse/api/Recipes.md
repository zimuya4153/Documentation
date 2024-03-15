# Recipes
使用Recipes类需要导入Recipes模块
导入示例：
```javascript
const { Recipes } = require('./GMLIB-LegacyRemoteCallApi/lib/GMLIB_API-JS');
```

### 注册无序合成表:

`Recipes.registerShapelessRecipe(
recipe_id: string,
ingredients: array<string>,
result: string,
count: int,
unlock: string
)`

参数:

- recipe_id: 合成表的唯一标识符。
- ingredients: 材料数组，表示无序排列。
- result: 合成结果。
- count: 合成结果的数量。
- unlock: 解锁条件，例如 "AlwaysUnlocked"。
  [JavaScript]

```JavaScript
Recipes.registerShapelessRecipe("groupmountain:quartz_recipe", ["minecraft:quartz_block"], "minecraft:quartz", 9, "AlwaysUnlocked");
```

### 注册有序合成表:

`Recipes.registerShapedRecipe(
recipe_id: string,
shape: array<string>,
ingredients: array<string>,
result: string,
count: int,
unlock: string
)`

参数:

- recipe_id: 合成表的唯一标识符。
- shape: 合成表的形状，数组元素为字符串。
- ingredients: 材料数组，按照形状排列。
- result: 合成结果。
- count: 合成结果的数量。
- unlock: 解锁条件，例如 "AlwaysUnlocked"。

[JavaScript]

```JavaScript
Recipes.registerShapedRecipe("groupmountain:reinforced_deepslate_recipe", ["ABA", "BBB", "ABA"], ["minecraft:echo_shard", "minecraft:deepslate"], "minecraft:reinforced_deepslate", 1, "AlwaysUnlocked");
```

### 注册熔炉合成表:

`Recipes.registerFurnaceRecipe(
recipe_id: string,
input: string,
output: string,
tags: array<string>
)`

参数:

- recipe_id : 合成表的唯一标识符。
- input : 输入材料。
- output : 合成结果。
- tags (array<string>): 材料的标签数组。
  [JavaScript]

```JavaScript
Recipes.registerFurnaceRecipe("recipe_id", "input", "output", ["tag1", "tag2"])
```

### 注册酿造混合表:

`Recipes.registerBrewingMixRecipe(
recipe_id: string,
input: string,
output: string,
reagent: string
)`

参数:

- recipe_id : 合成表的唯一标识符。
- input : 输入物品。
- output : 合成结果。
- reagent : 使用的药剂。
  [JavaScript]

```JavaScript
Recipes.registerBrewingMixRecipe("recipe_id", "input", "output", "reagent")
```

### 注册酿造容器表:

`Recipes.registerBrewingContainerRecipe(
recipe_id: string,
input: string,
output: string,
reagent: string
)`

参数:

- recipe_id : 合成表的唯一标识符。
- input : 输入物品。
- output : 合成结果。
- reagent : 使用的药剂。

[JavaScript]

```JavaScript
Recipes.registerBrewingContainerRecipe("recipe_id", "input", "output", "reagent")
```

### 注册锻造变形表:

`Recipes.registerSmithingTransformRecipe(
recipe_id: string,
smithing_template: string,
base: string,
addition: string,
result: string
)`

参数:

- recipe_id : 合成表的唯一标识符。
- smithing_template : 锻造模板。
- base : 基础物品。
- addition : 附加物品。
- result : 合成结果。

[JavaScript]

```JavaScript
Recipes.registerSmithingTransformRecipe("recipe_id", "template", "base", "addition", "result")
```

### 注册锻造修剪表:

`Recipes.registerSmithingTrimRecipe(
recipe_id: string,
smithing_template: string,
base: string,
addition: string
)`

参数:

- recipe_id : 合成表的唯一标识符。
- smithing_template : 锻造模板。
- base : 基础物品。
- addition : 附加物品。

[JavaScript]

```JavaScript
Recipes.registerSmithingTrimRecipe("recipe_id", "template", "base", "addition")
```

### 注册切石机合成表:

`Recipes.registerStoneCutterRecipe(
recipe_id: string,
input: string,
input_data: int,
output: string,
output_data: int,
output_count: int
)`

参数:

- recipe_id : 合成表的唯一标识符。
- input : 输入物品。
- input_data: 输入物品的额外数据。
- output : 合成结果。
- output_data: 合成结果的额外数据。
- output_count: 合成结果的数量。

[JavaScript]

```JavaScript
Recipes.registerStoneCutterRecipe("recipe_id", "input", 0, "output", 0, 1)
```

### 错误方块清理:

`Recipes.setUnknownBlockCleaner()`

[JavaScript]

```JavaScript
Recipes.setUnknownBlockCleaner()
实验性:
```

### 注册实验要求:

`Recipes.registerExperimentsRequire(experiment_id: int)`

参数:

- experiment_id: 实验的唯一标识符。

[JavaScript]

```JavaScript
Recipes.registerExperimentsRequire(6)
```

### 设置实验启用状态:

`Recipes.setExperimentEnabled(experiment_id: int, value: bool)`

参数:

- experiment_id: 实验的唯一标识符。
- value: 启用或禁用实验。
  [JavaScript]

```JavaScript
Recipes.setExperimentEnabled(6, true)
```

### 获取实验启用状态:

`Recipes.getExperimentEnabled(experiment_id: int)`

参数:

- experiment_id: 实验的唯一标识符。
- 返回值：bool
  [JavaScript]

```JavaScript
var isEnabled = Recipes.getExperimentEnabled(123)
```