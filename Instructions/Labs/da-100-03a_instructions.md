﻿

### ラボ 03A

Power BI Desktop へのデータの読み込み

# 概要

**ラボを完了するための所要時間は 45 分です**

この演習では、前のラボで作成した各クエリに変換を適用します。次に、クエリを適用して、各クエリをテーブルとしてデータ モデルに読み込みます。

このラボでは、次の方法を学習します:

* さまざまな変換を適用する

* クエリを適用してデータ モデルに読み込む

# 演習 1: データの読み込み

この演習では、前のラボで作成した各クエリに変換を適用します。

*前のラボを正常に完了した自信がない場合は、**D:\DA100\Lab02A\Solution** フォルダーにある前のラボのソリューション ファイルを開くことができます*。

### タスク 1: 営業担当者クエリを構成する

このタスクでは、**営業担当者**クエリを構成します。

1. 「**Power Query エディター**」 ウィンドウの 「**クエリ**」 ウィンドウで、**DimEmployee** クエリを選択します。     

    ![画像 1](Linked_image_Files/PowerBI_Lab03A_image1.png)

2. クエリの名前を変更するには、「**クエリ設定**」 ウィンドウ (右側) の 「**名前**」 ボックスで、テキストを **営業担当**に置き換えて、**Enter** キーを押 します。       

    *クエリ名はモデル テーブル名を決定します。簡潔でわかりやすい名前を定義することをお勧めします*。

3. 「**クエリ**」 ウィンドウで、クエリ名が更新されたことを確認します。 

    ![画像 87](Linked_image_Files/PowerBI_Lab03A_image2.png)

    *ここで、クエリ行をフィルター処理して、営業担当者である従業員のみを取得します*。

4. 特定の列を検索するには、「**ホーム**」 リボン タブの 「**列の管理**」 グループ内から 「**列の選択**」 をクリックし、「**列へ移動**」 を選択 します。       

    ![画像 88](Linked_image_Files/PowerBI_Lab03A_image3.png)

    *ヒント: この方法は、クエリに多数の列が含まれている場合に便利です。通常、列を見つけるために水平にスクロールすることができます*。

5. 「**列へ移動**」 ウィンドウで、列名順にリストを並べ替えるには、「**AZ**」 の並べ替えボタンをクリックし、「**名前**」 を選択します。     

    ![画像 94](Linked_image_Files/PowerBI_Lab03A_image4.png)

6. **SalesPersonFlag** 列を選択して、「**OK**」 をクリックします。

7. クエリをフィルタするには、「**SalesPersonFlag**」 列ヘッダーで下矢印をクリックし、「**FALSE**」 チェック ボックスをオフにします。   

    ![画像 95](Linked_image_Files/PowerBI_Lab03A_image5.png)

8. 「**OK**」 をクリックします。

    ![画像 96](Linked_image_Files/PowerBI_Lab03A_image6.png)

9. **クエリ設定** ウィンドウの 「**適用されるステップ**」 リストで、「**フィルターされた行**」 の手順が追加されていることに注目します。

    ![画像 98](Linked_image_Files/PowerBI_Lab03A_image7.png)

    *作成する各変換は、追加の手順ロジックが生成されます。ステップを編集または削除することができます。また、変換のその段階でクエリ結果をプレビューする手順を選択することもできます*。

10. 列を削除するには、「**ホーム**」 リボン タブの 「**列の管理**」 グループ内から **列の選択** アイコンをクリックします。

    ![画像 99](Linked_image_Files/PowerBI_Lab03A_image8.png)

11. **列の選択** ウィンドウで、すべての列のチェックを外す場合は、「**すべての列を選択**」 の項目をオフにします。   

    ![画像 102](Linked_image_Files/PowerBI_Lab03A_image9.png)

12. 列を含めるには、次の 6 つの列を確認します。

    * 従業員キー

    * EmployeeNationalIDAlternateKey

    * FirstName

    * LastName

    * タイトル

    * EmailAddress

13. 「**OK**」 をクリックします。

    ![画像 104](Linked_image_Files/PowerBI_Lab03A_image10.png)

14. 「**適用されるステップ**」 リストで、別のクエリ手順が追加されていることに注目してください。

    ![画像 112](Linked_image_Files/PowerBI_Lab03A_image11.png)

15. 単一の名前列を作成するには、最初に 「**FirstName**」 列ヘッダーを選択します。

16. **Ctrl** キーを押しながら、「**LastName**」 列を選択します。

    ![画像 116](Linked_image_Files/PowerBI_Lab03A_image12.png)

17. 選択列ヘッダーのいずれかを右クリックし、コンテキスト メニューの 「**列のマージ**」 を選択します。

    ![画像 117](Linked_image_Files/PowerBI_Lab03A_image13.png)

    *多くの一般的な変換は、列ヘッダーを右クリックし、コンテキスト メニューから選択することで適用できます。ただし、すべての変換 (およびそれ以上) は リボンで使用できることに注意してください*。

18. 「**列の結合**」 ウィンドウの 「**区切り記号**」 ボックスの一覧で、「**スペース**」 を選択します。 

19. 「**新しい列名**」 ボックスで、テキストを **営業担当者** に置き換えます。

    ![画像 119](Linked_image_Files/PowerBI_Lab03A_image14.png)

20. 「**OK**」 をクリックします。

    ![画像 5636](Linked_image_Files/PowerBI_Lab03A_image15.png)

21. **EmployeeNationalIDAlternateKey** 列の名前を変更するには、**EmployeeNationalIDAlternateKey** 列ヘッダーをダブルクリックします。

22. テキストを **EmployeeID** に置き換えて、**Enter** を押します。

    *列の名前を変更するように指示された場合、説明どおりに列の名前を正確に変更することが重要です*。

23. 前の手順を使用して、**電子メールアドレス**列の名前を **UPN** に変更します。

    *UPN は、ユーザー プリンシパル名の頭字語です。この列の値は、**ラボ 05A**で行レベルのセキュリティを設定するときに使用されます*。

24. 左下のステータス バーで、クエリに 5 列と 18 行が含まれているかどうかを確認します。

    ![画像 5638](Linked_image_Files/PowerBI_Lab03A_image16.png)

    *クエリで正しい結果が得られない場合は、後のラボを完了できなくなるため、先に進まないでください。正しい結果が表示されない場合は、このタスクの手順に戻って問題を修正してください*。

### タスク 2: SalespersonRegion クエリを構成する

このタスクでは、**SalespersonRegion** クエリを構成します。

1. 「**クエリ**」 ウィンドウで、「**DimEmployeeSalesTerritory**」 クエリを選択します。

    ![画像 5639](Linked_image_Files/PowerBI_Lab03A_image17.png)

2. 「**クエリの設定**」 ペインで、クエリの名前を **SalespersonRegion** に変更します。

3. 最後の 2 つの列を削除するには、最初に **DimEmployee** 列ヘッダーを選択します。

4. **Ctrl** キーを押しながら、**DimSalesTerritory** 列ヘッダーを選択します。

5. 選択した列ヘッダーのいずれかを右クリックし、コンテキスト メニューで 「**列を削除**」 を選択します。

    ![画像 5640](Linked_image_Files/PowerBI_Lab03A_image18.png)

6. ステータス バーで、クエリに 2列と 39 行があることを確認します。

    ![画像 5641](Linked_image_Files/PowerBI_Lab03A_image19.png)

### タスク 3: 製品クエリを構成する

このタスクでは、**製品**クエリを構成します。

*ラボで詳細な手順が既に提供されている場合、ラボの手順ではより簡潔な手順が提供されます。詳細な手順が必要な場合は、他のタスクを参照できます*。

1. **DimProduct** クエリを選択します。

    ![画像 5643](Linked_image_Files/PowerBI_Lab03A_image20.png)

2. クエリの名前を**製品**に変更します。

3. **FinishedGoodsFlag** 列を見つけ、列をフィルタリングして、完成品（つまり、TRUE）である製品を取得します。

4. 次の列を除くすべての列を削除します。

    * ProductKey

    * EnglishProductName

    * StandardCost

    * 色

    * DimProductSubcategory

5. **DimProductSubcategory** 列は関連テーブルを表していることに注意してください（**Value** リンクが含まれています）。

6. **DimProductSubcategory** 列ヘッダーの列名の右側にある 「展開」 ボタンをクリックします。 

    ![画像 5644](Linked_image_Files/PowerBI_Lab03A_image21.png)

7. すべての列をオフにするには、**（すべての列を選択）** の項目をオフにします。

8. **EnglishProductSubcategoryName** および **DimProductCategory** 列を確認します。

    ![画像 5646](Linked_image_Files/PowerBI_Lab03A_image22.png)

    *これらの 2 つの列を選択すると、変換が適用されて、**DimProductSubcategory** テーブルに結合され、これらの列が含まれます。**DimProductCategory** 列は、実際には別の関連テーブル*です。

9. 「**元の列名をプレフィックスとして使用します**」 チェックボックスをオフにします。

    ![画像 5647](Linked_image_Files/PowerBI_Lab03A_image23.png)

    *クエリ列名は常に一意である必要があります。このチェックボックスをオンにすると、各列の前に展開された列名が追加されます（この場合は **DimProductSubcategory**）。選択した列が**製品**クエリの列と衝突しないことがわかっているため、オプションは選択解除されています*。

10. 「**OK**」 をクリックします。

    ![画像 5648](Linked_image_Files/PowerBI_Lab03A_image24.png)

11. 変換によって 2 つの列が生成され、**DimProductCategory** 列が削除されていることに注意してください。

12. **DimProductCategory** を展開し、**EnglishProductCategoryName** 列のみを紹介します。

13. 次の 4 つの列の名前を変更します。

    * **EnglishProductName**から**製品**

    * **StandardCost**から**標準コスト** (スペースを含む) 

    * **EnglishProductSubcategoryName** から**サブカテゴリ**へ

    * **EnglishProductCategoryName** から**カテゴリ**へ

14. ステータス バーで、クエリに 6 つの列と 397 行があることを確認します。

    ![画像 5651](Linked_image_Files/PowerBI_Lab03A_image25.png)

### タスク 4: リセラー クエリを設定する

このタスクでは、**リセラー** クエリを構成します。

1. **DimReseller** クエリを選択します。 

    ![画像 5653](Linked_image_Files/PowerBI_Lab03A_image26.png)

2. クエリの名前を 「**リセラー**」 に変更します。

3. 次の列を除くすべての列を削除します。

    * ResellerKey

    * BusinessType

    * RellerName

    * DimGeography

4. 「**DimGeography**」 列を展開して、次の 3 つの列のみを含めます。

    * 市区町村

    * StateProvinceName

    * EnglishCountryRegionName

    ![画像 5656](Linked_image_Files/PowerBI_Lab03A_image27.png)

5. 「**ビジネス タイプ**」 列ヘッダーで、下向き矢印をクリックし、アイテムとウェアハウスの誤ったスペルを確認します。

    ![画像 2](Linked_image_Files/PowerBI_Lab03A_image28.png)

  
‎ 

6. 「**ビジネス タイプ**」 列ヘッダーを右クリックして、「**値の置換**」 を選択します。

    ![画像 4](Linked_image_Files/PowerBI_Lab03A_image29.png)

7. 「**値の置換**」 ウィンドウで、次の値を構成します。 

    * 「**検索する値**」 ボックスに「**ウェア ハウス**」と入力します。

    * 「**置換後の文字列**」 ボックスに「**倉庫**」と入力します。

    ![画像 5](Linked_image_Files/PowerBI_Lab03A_image30.png)

8. 「**OK**」 をクリックします。

    ![画像 6](Linked_image_Files/PowerBI_Lab03A_image31.png)

9. 次の 4 つの列の名前を変更します。

    * **BusinessType** 〜 **ビジネス タイプ** (スペースを含む)

    * **ResellerName** から**リセラー**へ

    * **StateProvinceName** から**都道府県**

    * **EnglishCountryRegionName** から**国の地域**

10. ステータス バーで、クエリに 6 列と 701 行が含まれているかどうかを確認します。

    ![画像 5657](Linked_image_Files/PowerBI_Lab03A_image32.png)

### タスク 5: 地域クエリを構成する

このタスクでは、**地域**クエリを設定します。

1. **DimSalesTerritory** クエリを選択します。

    ![画像 5659](Linked_image_Files/PowerBI_Lab03A_image33.png)

2. クエリの名前を 「**地域**」 に変更します。 

3. **SalesTerritoryAlternateKey** 列にフィルターを適用して、値 0 (ゼロ) を削除します。

    ![画像 5660](Linked_image_Files/PowerBI_Lab03A_image34.png)

4. 次の列を除くすべての列を削除します。

    * 営業地域キー

    * SalesTerritoryRegion

    * SalesTerritoryCountry

    * SalesTerritoryGroup

5. 次の 3 つの列の名前を変更します。

    * **SalesTerritoryRegion** から**リージョン**へ

    * **SalesTerritoryCountry** から**国**へ

    * **SalesTerritoryCountry** から**グループ**へ

6. ステータス バーで、クエリに 4 列と 10 行があることを確認します。

    ![画像 5661](Linked_image_Files/PowerBI_Lab03A_image35.png)

### タスク 6: 売上クエリを構成する

このタスクでは、**Sales** クエリを構成します。

1. **FactResellerSales** クエリを選択します。

    ![画像 5663](Linked_image_Files/PowerBI_Lab03A_image36.png)

2. クエリの名前を **Sales** に変更します。

3. 次の列を除くすべての列を削除します。

    * SalesOrderNumber

    * Orderdate

    * ProductKey

    * ResellerKey

    * 従業員キー

    * 営業地域キー

    * OrderQuantity

    * 単価

    * 総製品コスト

    * SalesAmount

    * DimProduct

    ***Lab 02A** で、**FactResellerSales** の行の一部に **TotalProductCost** の値が欠けていたことを思い出してください。不足している値を修正するために、製品の標準コストを取得するための **DimProduct** 列が含まれています*。

4. **DimProduct** 列を展開し、**StandardCost** 列を含めます。

5. カスタム列を作成するには、「**列を追加**」リボン タブの 「**全般**」 グループから、「**カスタム列**」 をクリックします。

    ![画像 5664](Linked_image_Files/PowerBI_Lab03A_image37.png)

6. **Custom Column** ウィンドウの **New Column Name** ボックスで、テキストを **Cost** に置き換えます。

    ![画像 5665](Linked_image_Files/PowerBI_Lab03A_image38.png)

7. 「**カスタム列の数式**」 ボックスに、次の式 (等号記号の後) を入力します。

8. **D:\DA100\Lab03A\Assets\Snippets.txt** ファイルから式をコピーすると便利です。

    **Power Query**

    ```
    if 「TotalProductCost」 = null then 「OrderQuantity」 * 「StandardCost」 else 「TotalProductCost」
    ```

    *この式は、**TotalProductCost** 値が欠落しているかどうかをテストします。そうであれば、**OrderQuantity** 値に **StandardCost** 値を掛けて値を生成します。 それ以外の場合は、既存の **TotalProductCost** 値*を使用します。

9. 「**OK**」 をクリックします。

    ![画像 5666](Linked_image_Files/PowerBI_Lab03A_image39.png)

10. 次の 2 つの列を削除します。

    * 総製品コスト

    * StandardCost

11. 次の 3 つの列の名前を変更します。

    * **OrderQuantity** から **Quantity**

    * **UnitPrice** から **Unitity** (スペースを含む)

    * **SalesAmount** から **Sales**

12. 列のデータ型を変更するには、 **列**名の左側にある 「数量」 列ヘッダーで 「**1.2**」 アイコンをクリック し、「**整数**」 を選択 します。     

    ![画像 5667](Linked_image_Files/PowerBI_Lab03A_image40.png)

    *正しいデータ型を構成することが重要です。列に数値が含まれている場合は、数学計算を実行する場合は、正しい型を選択することも重要です*。

13. 次の 3 つの列のデータ型を**固定 10 進数**に変更します。

    * 単価

    * 売上

    * 原価

    ![画像 5668](Linked_image_Files/PowerBI_Lab03A_image41.png)

    *固定 10 進数データ型は、値を完全な精度で格納するため、10 進数よりも多くのストレージ スペースが必要です。財務値、またはレート (為替レートなど) には、固定小数型を使用することが重要です*。

14. ステータス バーで、クエリに 10 列と 999+ 行があることを確認します。

    ![画像 5669](Linked_image_Files/PowerBI_Lab03A_image42.png)

    *各クエリのプレビュー データとして、最大 1000 行が読み込まれます*。

### タスク 7: ターゲット クエリを構成する

このタスクでは、**ターゲット** クエリを構成します。

1. 「**ResellerSalesTargets**」 クエリを選択します。

    ![画像 5672](Linked_image_Files/PowerBI_Lab03A_image43.png)

2. クエリの名前を「**ターゲット**」に変更します。 

3. 12 か月の列 (**M01 **-** M12**) のピボットを解除するには、最初に 「**年**」 および 「**従業員 ID**」 列ヘッダーを複数選択します。

    ![画像 5673](Linked_image_Files/PowerBI_Lab03A_image44.png)

4. 選択した列ヘッダーのいずれかを右クリックし、コンテキスト メニューで 「**他の列のピボット解除**」 を選択します。

    ![画像 5674](Linked_image_Files/PowerBI_Lab03A_image45.png)

5. 列名が 「**属性**」 列に表示され、値が 「**値**」 列に表示されることに注意してください。

6. ハイフン (-) 値を削除するために、「**値**」 列にフィルターを適用します。

7. 次の 2 つの列の名前を変更します。

    * **Attribute** から **MonthNumber** (2 つの単語の間にスペースはありません。後で削除されます）

    * **値**から**目標**

    *ここで、日付列を作成するために変換を適用します。日付は、「**Year**」 および 「**MonthNumber**」 列から取得されます。 **例の列**機能*を使用して列を作成します。

8. **MonthNumber** 列の値を準備するには、「**MonthNumber**」 列ヘッダーを右クリックしてから、「**値の置換**」 を選択します。

    ![画像 5676](Linked_image_Files/PowerBI_Lab03A_image46.png)

9. 「**値の置換**」 ウィンドウの 「**検索する値**」 ボックスに、「**M**」と入力します。

    ![画像 5677](Linked_image_Files/PowerBI_Lab03A_image47.png)

10. 「**OK**」 をクリックします。

11. 「**MonthNumber**」 列のデータ型を 「**整数**」 に変更します。   

    ![画像 5678](Linked_image_Files/PowerBI_Lab03A_image48.png)

12. 「**列を追加**」リボンタブの 「**全般**」 グループ内から、「**例の列**」 アイコンをクリックします。  

    ![画像 5675](Linked_image_Files/PowerBI_Lab03A_image49.png)

13. 最初の行は年 **2017** と月番号 **7** であることに注意してください。 

14. 「**列 1**」 列の最初のグリッド セルに、「**7/1/2017**」と入力してから 、**Enter** キーを押します。     

    *仮想マシンは米国の地域設定を使用しているため、この日付は実際には 2017 年 7 月 1 日です。*

15. グリッド セルが予測値で更新されることに注意してください。

    この機能では、2 つの列の値を組み合わせることを正確に予測しています。

16. クエリ グリッドの上に表示される数式も確認してください。

    ![画像 5679](Linked_image_Files/PowerBI_Lab03A_image50.png)

17. 新しい列の名前を変更するには、「**結合**」 列ヘッダーをダブルクリックします。

18. 列の名前を **TargetMonth** に変更します。 

    ![画像 5680](Linked_image_Files/PowerBI_Lab03A_image51.png)

19. 「**OK**」 をクリックします。

    ![画像 5681](Linked_image_Files/PowerBI_Lab03A_image52.png)

20. 次のコードを削除します。

    * 年

    * MonthNumber

21. 次の列のデータ型を変更します。

    * 固定 10 進数としての**目標**

    * 日付としての **TargetMonth**

22. **目標**値に 1000 を掛けるには、「**ターゲット**」 列ヘッダーを選択し 、「**変換**」 リボン タブの 「**数値列**」 グループ内で 「**標準**」 をクリックし、「**乗算**」 を選択します。

    ![画像 5682](Linked_image_Files/PowerBI_Lab03A_image53.png)

23. 「**乗算**」 ウィンドウの 「**値**」 ボックスに「**1000**」と入力します。

    ![画像 5683](Linked_image_Files/PowerBI_Lab03A_image54.png)

24. 「**OK**」 をクリックします。

    ![画像 5684](Linked_image_Files/PowerBI_Lab03A_image55.png)

25. ステータスバーで、クエリに 3 つの列と 809 行があることを確認します。

    ![画像 5685](Linked_image_Files/PowerBI_Lab03A_image56.png)

### タスク 8: ColorFormats クエリを構成する

このタスクでは、**ColorFormats** クエリを構成します。

1. **ColorFormats** クエリを選択します。   
	![画像 5687](Linked_image_Files/PowerBI_Lab03A_image57.png)

2. 最初の行に列名が含まれていることに注意してください。

3. 「**ホーム**」 リボン タブの 「**変換**」 グループ内で、「**先頭行をヘッダーとして使用**」 をクリックします。  
    ![画像 5688](Linked_image_Files/PowerBI_Lab03A_image58.png)

4. ステータス バーで、クエリに 3 列と 10 行があることを確認します。  
	![画像 5689](Linked_image_Files/PowerBI_Lab03A_image59.png)

### タスク 9: 製品クエリを更新する

このタスクでは、**ColorFormats** クエリをマージして、**Product** クエリを更新します。

1. **製品**クエリを選択します。  
	![画像 5690](Linked_image_Files/PowerBI_Lab03A_image60.png)

1. **ColorFormats** クエリをマージするには、「**ホーム**」 リボン タブの 「**結合**」 グループ内から、「**クエリのマージ**」 をクリックします。  
	![画像 5654](Linked_image_Files/PowerBI_Lab03A_image61.png)  
	*クエリをマージすると、異なるデータ ソース (SQL サーバーと CSV ファイル) からのデータを統合できます*。

1. 「**マージ**」 ウィンドウの 「**製品**」 クエリ グリッドで、「**色**」 列ヘッダーを選択 します。       
	![画像 5655](Linked_image_Files/PowerBI_Lab03A_image62.png)

1. 「**製品**」 クエリ グリッドの下のドロップダウン リストで、「**色の書式**」 クエリを選択します。

1. 「**ColorFormats**」 クエリ グリッドで、「**Color**」 列ヘッダーを選択します。  

1. 「**プライバシー レベル**」 ウィンドウが開いたら、2 つのデータ ソースそれぞれに対して、対応するドロップダウン リストで、「**組織**」 を選択します。  
	![画像 5691](Linked_image_Files/PowerBI_Lab03A_image63.png)  
	*データ ソースのプライバシー レベルを構成して、データをソース間で共有できるかどうかを決定できます。各データソースを**組織**に設定すると、必要に応じてデータを共有できます。プライベート データ ソースを他のデータ ソースと共有することはできません。プライベート データを共有できないという意味ではありません。 つまり、Power Query エンジンはソース間でデータを共有できません*。

1. 「**保存**」 をクリックします。  
	![画像 5692](Linked_image_Files/PowerBI_Lab03A_image64.png)

1. **マージ** ウィンドウで、「**OK**」 をクリックします。  
	![画像 5693](Linked_image_Files/PowerBI_Lab03A_image65.png)

1. 「**ColorFormats**」 列を展開して、次の 2 つの列を含めます。 
    * 背景色の選択  
    * フォントの色の書式

	![画像 5694](Linked_image_Files/PowerBI_Lab03A_image66.png)

1. ステータス バーで、クエリに 8 つの列と 397 の行があることを確認します。  
	![画像 5695](Linked_image_Files/PowerBI_Lab03A_image67.png)

### タスク 10: ColorFormats クエリを更新する

このタスクでは、**ColorFormats** を更新してロードを無効にします。

1. **ColorFormats** クエリを選択します。   
	![画像 321](Linked_image_Files/PowerBI_Lab03A_image68.png)

2. 「**クエリ設定**」 ペインで、「**すべてのプロパティ**」 リンクをクリックします。     
	![画像 322](Linked_image_Files/PowerBI_Lab03A_image69.png)

3. 「**クエリのプロパティ**」 ウィンドウで、「**レポートへの読み込みを有効にする**」 チェック ボックスをオフにします。     
	![画像 323](Linked_image_Files/PowerBI_Lab03A_image70.png)  
	*ロードを無効にすると、データ モデルにテーブルとして読み込まれません。これは、クエリが Product クエリとマージされたために行われます。これにより、データ モデルに対応できます*。

4. 「**OK**」 をクリックします。  
	![画像 324](Linked_image_Files/PowerBI_Lab03A_image71.png)

### 仕上げ

このタスクでは、ラボを完了します。

1. 次のように正しく名前が付けられた 8 つのクエリがあることを確認します。

    * 営業担当者

    * SalespersonRegion

    * 製品

    * リセラー

    * リージョン

    * 売上

    * ターゲット

    * ColorFormats  (データモデルに読み込まれません)

2. データ モデルを読み込むには、「**ファイル**」 バックステージ ビューで 「**閉じる**」 を選択します。     
	![画像 326](Linked_image_Files/PowerBI_Lab03A_image72.png)  
	*これで、すべての読み込み可能なクエリがデータ モデル に読み込まれます*。

3. 「**フィールド**」 ウィンドウ (右側) で、データ モデルに読み込まれた 7 つのテーブルに注目します。  
	![画像 3](Linked_image_Files/PowerBI_Lab03A_image73.png)

4. Power BI Desktop ファイルを保存します。

5. Power BI Desktop を開いたままにしておきます。  
	*次の演習では、データ モデル テーブルとリレーションシップを構成します*。
