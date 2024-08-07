# STORAGE

本节指定Cuberite是否应该保存world区块，以及world文件的压缩级别。

## 可选选项

| 变量              | 定义                                                                                                                                                        | 默认值  |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| Schema            | 指定是否应保存世界块。可能是“Default”、“Anvil”和“Forgetful”之一。有关其描述，请参见下表。                                                                            | Default |
| CompressionFactor | 世界文件应该进行多少压缩。 较低的值意味着文件大小更大，但性能略有提升； 较高的值意味着文件大小略小，但性能也会随之降低。 建议保持默认设置即可。 | 6       |

## 保存模式

| SCHEMA    | 文件类型 | 描述                                                                                                                                                      |
| --------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Default   | .mca     | 目前这只是Anvil的别名。                                                                                                                                   |
| Anvil     | .mca     | 保存区块。存储方式与其他与Minecraft相关的工具和程序兼容。 MCA文件存储在世界文件夹的"region"子文件夹中， 并在世界文件夹内生成一个"level.dat"文件。 |
| Forgetful | N/A      | 不能保存数据块。一旦区块被卸载，对世界的更改就会丢失， 这对于只读的公共服务器很有用。 请注意，Cuberite仍然会使用其他模式加载块。                      |
