# Draw 專案

> 紀錄一些繪圖，順便把github當成雲端硬碟用...

## 資料夾結構
```
+--- Draw
     +--- README.md                      說明文件
     +--- Autocad
     +--- Blender
     +--- Drawio
     +--- Photoshop
     +--- Sketchup
     +--- Illustrator
          +--- Note                           筆記
          +--- Record                         作品
          +--- Templet                        範本檔案
          +--- ClothinAndAccessories          服飾、配件
          +--- Print                          列印用
          +--- Tracing                        描圖
```

## `Git LFS`教學
> 過大的檔案要用Git LFS，常用於設計檔案，二進制檔案。

1. 常用副檔名
    * AutoCAD 的主要副檔名：
      * .dwg (主要的 AutoCAD 繪圖檔案格式)
      * .dxf (Drawing Exchange Format，用於交換的格式)
      * .dwt (AutoCAD 範本檔)
    * Blender 的主要副檔名：
      * .blend (Blender 的原生檔案格式)
      * .blend1 (自動備份檔案)
    * Draw.io 的主要副檔名：
      * .drawio (Draw.io 的原生檔案格式)
      * .xml (可匯出的 XML 格式)
      * .png (可包含圖表數據的 PNG 圖片)
      * .svg (可編輯的向量圖形格式)
    * Photoshop 的主要副檔名：
      * .psd (Photoshop 的原生檔案格式)
      * .psb (大型文件格式)
    * SketchUp 的主要副檔名：
      * .skp (SketchUp 的原生檔案格式)
      * .skb (SketchUp 備份檔)
    * Illustrator 的主要副檔名：
      * .ai (Illustrator 的原生檔案格式)
      * .eps (封裝式 PostScript 格式)
2. 安裝 Git-lfs
     ```ps1
     # 安裝git就會附帶lfs功能
     winget install -e --id Git.Git
     ```
3. 加入追蹤設定`.gitattributes`
   > 選擇您希望 Git LFS 管理的文件類型，或直接編輯 .gitattributes。
   * 初始化
     ``` bash
     git init
     ```
   * 以`git lfs`追蹤副檔名，此動作將生成`.gitattributes`
     ``` sh
     git lfs track "*.dwg"
     git lfs track "*.dxf"
     git lfs track "*.blend"
     git lfs track "*.drawio"
     git lfs track "*.svg"
     git lfs track "*.psd"
     git lfs track "*.skp"
     git lfs track "*.ai"
     ```
   * 追蹤設定加入
     ``` sh
     git add .
     ```
   * 推至儲存庫
     ``` sh
     git remote add origin https://github.com/orange9982239/Draw.git
     git branch -M main
     git push -u origin main
     ```
## 參考
   * https://git-lfs.github.com/