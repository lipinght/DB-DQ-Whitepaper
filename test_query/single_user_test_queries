## S1 Q1
// DAX Query
DEFINE
    VAR __DS0FilterTable = 
        FILTER(
            KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
            'catalog_sales'[cache_buster] < 2
        )

    VAR __DS0FilterTable2 = 
        FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

EVALUATE
    SUMMARIZECOLUMNS(
        __DS0FilterTable,
        __DS0FilterTable2,
        "Store_Distinct_Customers", IGNORE('Measures 1'[Store Distinct Customers])
    )
## S2 Q1
// DAX Query
DEFINE
    VAR __DS0FilterTable = 
        TREATAS({"CO"}, 'customer_address'[ca_state])

    VAR __DS0FilterTable2 = 
        TREATAS({"Advanced Degree"}, 'customer_demographics'[cd_education_status])

    VAR __DS0FilterTable3 = 
        TREATAS({"'date_dim'[d_quarter_name]"}, 'Time Unit'[Time Unit Fields])

    VAR __DS0FilterTable4 = 
        FILTER(
            KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
            'catalog_sales'[cache_buster] < 2
        )

    VAR __DS0FilterTable5 = 
        FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

EVALUATE
    SUMMARIZECOLUMNS(
        __DS0FilterTable,
        __DS0FilterTable2,
        __DS0FilterTable3,
        __DS0FilterTable4,
        __DS0FilterTable5,
        "Store_Distinct_Customers", IGNORE('Measures 1'[Store Distinct Customers])
    )
## S3 Q1
// DAX Query
DEFINE
	VAR __DS0FilterTable = 
		TREATAS({"CA"}, 'customer_address'[ca_state])

	VAR __DS0FilterTable2 = 
		TREATAS({"College"}, 'customer_demographics'[cd_education_status])

	VAR __DS0FilterTable3 = 
		TREATAS({"Brett Yates"}, 'store'[s_manager])

	VAR __DS0FilterTable4 = 
		TREATAS({"DHL"}, 'ship_mode'[sm_carrier])

	VAR __DS0FilterTable5 = 
		TREATAS({"quarterly"}, 'catalog_page'[cp_type])

	VAR __DS0FilterTable6 = 
		TREATAS({"'date_dim'[d_quarter_name]"}, 'Time Unit'[Time Unit Fields])

	VAR __DS0FilterTable7 = 
		TREATAS({2026}, 'date_dim'[d_year])

	VAR __DS0FilterTable8 = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __DS0FilterTable9 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

EVALUATE
	SUMMARIZECOLUMNS(
		__DS0FilterTable,
		__DS0FilterTable2,
		__DS0FilterTable3,
		__DS0FilterTable4,
		__DS0FilterTable5,
		__DS0FilterTable6,
		__DS0FilterTable7,
		__DS0FilterTable8,
		__DS0FilterTable9,
		"Store_Distinct_Customers", IGNORE('Measures 1'[Store Distinct Customers])
	)


## S1 Q2
// DAX Query
DEFINE
	VAR __DS0FilterTable = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __DS0FilterTable2 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

	VAR __DS0Core = 
		SUMMARIZECOLUMNS(
			'item'[i_category],
			__DS0FilterTable,
			__DS0FilterTable2,
			"Store_Profit___by_Item_Category", 'Measures 1'[Store Profit % by Item Category]
		)

	VAR __DS0BodyLimited = 
		TOPN(1002, __DS0Core, [Store_Profit___by_Item_Category], 0, 'item'[i_category], 1)

EVALUATE
	__DS0BodyLimited

ORDER BY
	[Store_Profit___by_Item_Category] DESC, 'item'[i_category]


## S2 Q2
// DAX Query
DEFINE
	VAR __DS0FilterTable = 
		TREATAS({"CO"}, 'customer_address'[ca_state])

	VAR __DS0FilterTable2 = 
		TREATAS({"Advanced Degree"}, 'customer_demographics'[cd_education_status])

	VAR __DS0FilterTable3 = 
		TREATAS({"'date_dim'[d_quarter_name]"}, 'Time Unit'[Time Unit Fields])

	VAR __DS0FilterTable4 = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __DS0FilterTable5 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

	VAR __DS0Core = 
		SUMMARIZECOLUMNS(
			'item'[i_category],
			__DS0FilterTable,
			__DS0FilterTable2,
			__DS0FilterTable3,
			__DS0FilterTable4,
			__DS0FilterTable5,
			"Store_Profit___by_Item_Category", 'Measures 1'[Store Profit % by Item Category]
		)

	VAR __DS0BodyLimited = 
		TOPN(1002, __DS0Core, [Store_Profit___by_Item_Category], 0, 'item'[i_category], 1)

EVALUATE
	__DS0BodyLimited

ORDER BY
	[Store_Profit___by_Item_Category] DESC, 'item'[i_category]


## S3 Q2
// DAX Query
DEFINE
	VAR __DS0FilterTable = 
		TREATAS({"CA"}, 'customer_address'[ca_state])

	VAR __DS0FilterTable2 = 
		TREATAS({"College"}, 'customer_demographics'[cd_education_status])

	VAR __DS0FilterTable3 = 
		TREATAS({"Brett Yates"}, 'store'[s_manager])

	VAR __DS0FilterTable4 = 
		TREATAS({"DHL"}, 'ship_mode'[sm_carrier])

	VAR __DS0FilterTable5 = 
		TREATAS({"quarterly"}, 'catalog_page'[cp_type])

	VAR __DS0FilterTable6 = 
		TREATAS({"'date_dim'[d_quarter_name]"}, 'Time Unit'[Time Unit Fields])

	VAR __DS0FilterTable7 = 
		TREATAS({2026}, 'date_dim'[d_year])

	VAR __DS0FilterTable8 = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __DS0FilterTable9 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

	VAR __DS0Core = 
		SUMMARIZECOLUMNS(
			'item'[i_category],
			__DS0FilterTable,
			__DS0FilterTable2,
			__DS0FilterTable3,
			__DS0FilterTable4,
			__DS0FilterTable5,
			__DS0FilterTable6,
			__DS0FilterTable7,
			__DS0FilterTable8,
			__DS0FilterTable9,
			"Store_Profit___by_Item_Category", 'Measures 1'[Store Profit % by Item Category]
		)

	VAR __DS0BodyLimited = 
		TOPN(1002, __DS0Core, [Store_Profit___by_Item_Category], 0, 'item'[i_category], 1)

EVALUATE
	__DS0BodyLimited

ORDER BY
	[Store_Profit___by_Item_Category] DESC, 'item'[i_category]


## S1 Q3
// DAX Query
DEFINE
	COLUMN '__SQDS0VisualCalcs'[Rank] = 
		(/* USER DAX BEGIN */
Rank(ORDERBY([Catalog Revenue],Desc))
/* USER DAX END */)

	VAR __SQDS0FilterTable = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __SQDS0FilterTable2 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

	VAR __SQDS0Core = 
		SUMMARIZECOLUMNS(
			ROLLUPADDISSUBTOTAL('promotion'[p_promo_name], "IsSQDS0GrandTotalRowTotal"),
			__SQDS0FilterTable,
			__SQDS0FilterTable2,
			"Catalog_Revenue", 'Measures 1'[Catalog Revenue]
		)

	VAR __SQDS0VisualCalcsInput = 
		SELECTCOLUMNS(
			KEEPFILTERS(
				SELECTCOLUMNS(
					__SQDS0Core,
					"p_promo_name", 'promotion'[p_promo_name],
					"IsSQDS0GrandTotalRowTotal", [IsSQDS0GrandTotalRowTotal],
					"Catalog_Revenue", [Catalog_Revenue]
				)
			),
			"p_promo_name", [p_promo_name],
			"IsSQDS0GrandTotalRowTotal", [IsSQDS0GrandTotalRowTotal],
			"Catalog Revenue", [Catalog_Revenue]
		)

	TABLE '__SQDS0VisualCalcs' = 
		__SQDS0VisualCalcsInput
		WITH VISUAL SHAPE
			AXIS rows
				GROUP [p_promo_name] TOTAL [IsSQDS0GrandTotalRowTotal]
				ORDER BY
					[p_promo_name] ASC
			DENSIFY "IsDensifiedRow"

	VAR __SQDS0RemoveEmptyDensified = 
		FILTER(
			KEEPFILTERS('__SQDS0VisualCalcs'),
			OR(
				NOT('__SQDS0VisualCalcs'[IsDensifiedRow]),
				NOT(ISBLANK('__SQDS0VisualCalcs'[Rank]))
			)
		)

	VAR __DS0Core = 
		SELECTCOLUMNS(
			KEEPFILTERS(
				FILTER(
					KEEPFILTERS(__SQDS0RemoveEmptyDensified),
					'__SQDS0VisualCalcs'[IsSQDS0GrandTotalRowTotal] = FALSE
				)
			),
			"'__SQDS0VisualCalcs'[p_promo_name]", '__SQDS0VisualCalcs'[p_promo_name],
			"'__SQDS0VisualCalcs'[Rank]", '__SQDS0VisualCalcs'[Rank],
			"'__SQDS0VisualCalcs'[Catalog Revenue]", '__SQDS0VisualCalcs'[Catalog Revenue]
		)

	VAR __DS0PrimaryWindowed = 
		TOPN(
			1001,
			__DS0Core,
			'__SQDS0VisualCalcs'[Catalog Revenue],
			0,
			'__SQDS0VisualCalcs'[p_promo_name],
			1
		)

EVALUATE
	GROUPBY(
		__DS0Core,
		"MinRank", MINX(CURRENTGROUP(), '__SQDS0VisualCalcs'[Rank]),
		"MaxRank", MAXX(CURRENTGROUP(), '__SQDS0VisualCalcs'[Rank])
	)

EVALUATE
	__DS0PrimaryWindowed

ORDER BY
	'__SQDS0VisualCalcs'[Catalog Revenue] DESC, '__SQDS0VisualCalcs'[p_promo_name]


## S2 Q3
// DAX Query
DEFINE
	COLUMN '__SQDS0VisualCalcs'[Rank] = 
		(/* USER DAX BEGIN */
Rank(ORDERBY([Catalog Revenue],Desc))
/* USER DAX END */)

	VAR __SQDS0FilterTable = 
		TREATAS({"CO"}, 'customer_address'[ca_state])

	VAR __SQDS0FilterTable2 = 
		TREATAS({"Advanced Degree"}, 'customer_demographics'[cd_education_status])

	VAR __SQDS0FilterTable3 = 
		TREATAS({"'date_dim'[d_quarter_name]"}, 'Time Unit'[Time Unit Fields])

	VAR __SQDS0FilterTable4 = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __SQDS0FilterTable5 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

	VAR __SQDS0Core = 
		SUMMARIZECOLUMNS(
			ROLLUPADDISSUBTOTAL('promotion'[p_promo_name], "IsSQDS0GrandTotalRowTotal"),
			__SQDS0FilterTable,
			__SQDS0FilterTable2,
			__SQDS0FilterTable3,
			__SQDS0FilterTable4,
			__SQDS0FilterTable5,
			"Catalog_Revenue", 'Measures 1'[Catalog Revenue]
		)

	VAR __SQDS0VisualCalcsInput = 
		SELECTCOLUMNS(
			KEEPFILTERS(
				SELECTCOLUMNS(
					__SQDS0Core,
					"p_promo_name", 'promotion'[p_promo_name],
					"IsSQDS0GrandTotalRowTotal", [IsSQDS0GrandTotalRowTotal],
					"Catalog_Revenue", [Catalog_Revenue]
				)
			),
			"p_promo_name", [p_promo_name],
			"IsSQDS0GrandTotalRowTotal", [IsSQDS0GrandTotalRowTotal],
			"Catalog Revenue", [Catalog_Revenue]
		)

	TABLE '__SQDS0VisualCalcs' = 
		__SQDS0VisualCalcsInput
		WITH VISUAL SHAPE
			AXIS rows
				GROUP [p_promo_name] TOTAL [IsSQDS0GrandTotalRowTotal]
				ORDER BY
					[p_promo_name] ASC
			DENSIFY "IsDensifiedRow"

	VAR __SQDS0RemoveEmptyDensified = 
		FILTER(
			KEEPFILTERS('__SQDS0VisualCalcs'),
			OR(
				NOT('__SQDS0VisualCalcs'[IsDensifiedRow]),
				NOT(ISBLANK('__SQDS0VisualCalcs'[Rank]))
			)
		)

	VAR __DS0Core = 
		SELECTCOLUMNS(
			KEEPFILTERS(
				FILTER(
					KEEPFILTERS(__SQDS0RemoveEmptyDensified),
					'__SQDS0VisualCalcs'[IsSQDS0GrandTotalRowTotal] = FALSE
				)
			),
			"'__SQDS0VisualCalcs'[p_promo_name]", '__SQDS0VisualCalcs'[p_promo_name],
			"'__SQDS0VisualCalcs'[Rank]", '__SQDS0VisualCalcs'[Rank],
			"'__SQDS0VisualCalcs'[Catalog Revenue]", '__SQDS0VisualCalcs'[Catalog Revenue]
		)

	VAR __DS0PrimaryWindowed = 
		TOPN(
			1001,
			__DS0Core,
			'__SQDS0VisualCalcs'[Catalog Revenue],
			0,
			'__SQDS0VisualCalcs'[p_promo_name],
			1
		)

EVALUATE
	GROUPBY(
		__DS0Core,
		"MinRank", MINX(CURRENTGROUP(), '__SQDS0VisualCalcs'[Rank]),
		"MaxRank", MAXX(CURRENTGROUP(), '__SQDS0VisualCalcs'[Rank])
	)

EVALUATE
	__DS0PrimaryWindowed

ORDER BY
	'__SQDS0VisualCalcs'[Catalog Revenue] DESC, '__SQDS0VisualCalcs'[p_promo_name]


## S3 Q3
// DAX Query
DEFINE
	COLUMN '__SQDS0VisualCalcs'[Rank] = 
		(/* USER DAX BEGIN */
Rank(ORDERBY([Catalog Revenue],Desc))
/* USER DAX END */)

	VAR __SQDS0FilterTable = 
		TREATAS({"CA"}, 'customer_address'[ca_state])

	VAR __SQDS0FilterTable2 = 
		TREATAS({"College"}, 'customer_demographics'[cd_education_status])

	VAR __SQDS0FilterTable3 = 
		TREATAS({"Brett Yates"}, 'store'[s_manager])

	VAR __SQDS0FilterTable4 = 
		TREATAS({"DHL"}, 'ship_mode'[sm_carrier])

	VAR __SQDS0FilterTable5 = 
		TREATAS({"quarterly"}, 'catalog_page'[cp_type])

	VAR __SQDS0FilterTable6 = 
		TREATAS({"'date_dim'[d_quarter_name]"}, 'Time Unit'[Time Unit Fields])

	VAR __SQDS0FilterTable7 = 
		TREATAS({2026}, 'date_dim'[d_year])

	VAR __SQDS0FilterTable8 = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __SQDS0FilterTable9 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

	VAR __SQDS0Core = 
		SUMMARIZECOLUMNS(
			ROLLUPADDISSUBTOTAL('promotion'[p_promo_name], "IsSQDS0GrandTotalRowTotal"),
			__SQDS0FilterTable,
			__SQDS0FilterTable2,
			__SQDS0FilterTable3,
			__SQDS0FilterTable4,
			__SQDS0FilterTable5,
			__SQDS0FilterTable6,
			__SQDS0FilterTable7,
			__SQDS0FilterTable8,
			__SQDS0FilterTable9,
			"Catalog_Revenue", 'Measures 1'[Catalog Revenue]
		)

	VAR __SQDS0VisualCalcsInput = 
		SELECTCOLUMNS(
			KEEPFILTERS(
				SELECTCOLUMNS(
					__SQDS0Core,
					"p_promo_name", 'promotion'[p_promo_name],
					"IsSQDS0GrandTotalRowTotal", [IsSQDS0GrandTotalRowTotal],
					"Catalog_Revenue", [Catalog_Revenue]
				)
			),
			"p_promo_name", [p_promo_name],
			"IsSQDS0GrandTotalRowTotal", [IsSQDS0GrandTotalRowTotal],
			"Catalog Revenue", [Catalog_Revenue]
		)

	TABLE '__SQDS0VisualCalcs' = 
		__SQDS0VisualCalcsInput
		WITH VISUAL SHAPE
			AXIS rows
				GROUP [p_promo_name] TOTAL [IsSQDS0GrandTotalRowTotal]
				ORDER BY
					[p_promo_name] ASC
			DENSIFY "IsDensifiedRow"

	VAR __SQDS0RemoveEmptyDensified = 
		FILTER(
			KEEPFILTERS('__SQDS0VisualCalcs'),
			OR(
				NOT('__SQDS0VisualCalcs'[IsDensifiedRow]),
				NOT(ISBLANK('__SQDS0VisualCalcs'[Rank]))
			)
		)

	VAR __DS0Core = 
		SELECTCOLUMNS(
			KEEPFILTERS(
				FILTER(
					KEEPFILTERS(__SQDS0RemoveEmptyDensified),
					'__SQDS0VisualCalcs'[IsSQDS0GrandTotalRowTotal] = FALSE
				)
			),
			"'__SQDS0VisualCalcs'[p_promo_name]", '__SQDS0VisualCalcs'[p_promo_name],
			"'__SQDS0VisualCalcs'[Rank]", '__SQDS0VisualCalcs'[Rank],
			"'__SQDS0VisualCalcs'[Catalog Revenue]", '__SQDS0VisualCalcs'[Catalog Revenue]
		)

	VAR __DS0PrimaryWindowed = 
		TOPN(
			1001,
			__DS0Core,
			'__SQDS0VisualCalcs'[Catalog Revenue],
			0,
			'__SQDS0VisualCalcs'[p_promo_name],
			1
		)

EVALUATE
	GROUPBY(
		__DS0Core,
		"MinRank", MINX(CURRENTGROUP(), '__SQDS0VisualCalcs'[Rank]),
		"MaxRank", MAXX(CURRENTGROUP(), '__SQDS0VisualCalcs'[Rank])
	)

EVALUATE
	__DS0PrimaryWindowed

ORDER BY
	'__SQDS0VisualCalcs'[Catalog Revenue] DESC, '__SQDS0VisualCalcs'[p_promo_name]


## S1 Q4
// DAX Query
DEFINE
    VAR __DS0FilterTable = 
        FILTER(
            KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
            'catalog_sales'[cache_buster] < 2
        )

    VAR __DS0FilterTable2 = 
        FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

    VAR __DS0Core = 
        SUMMARIZECOLUMNS(
            'date_dim'[d_quarter_name],
            __DS0FilterTable,
            __DS0FilterTable2,
            "Catalog_Sales_Quantity", 'Measures 1'[Catalog Sales Quantity],
            "Catalog_Sales_Same_Period_LY", 'Measures 1'[Catalog Sales Same Period LY],
            "Catalog_Sales_YoY", 'Measures 1'[Catalog Sales YoY]
        )

    VAR __DS0PrimaryWindowed = 
        TOPN(1001, __DS0Core, 'date_dim'[d_quarter_name], 0)

EVALUATE
    __DS0PrimaryWindowed

ORDER BY
    'date_dim'[d_quarter_name] DESC

## S2 Q4
// DAX Query
DEFINE
	VAR __DS0FilterTable = 
		TREATAS({"CO"}, 'customer_address'[ca_state])

	VAR __DS0FilterTable2 = 
		TREATAS({"Advanced Degree"}, 'customer_demographics'[cd_education_status])

	VAR __DS0FilterTable3 = 
		TREATAS({"'date_dim'[d_quarter_name]"}, 'Time Unit'[Time Unit Fields])

	VAR __DS0FilterTable4 = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __DS0FilterTable5 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

	VAR __DS0Core = 
		SUMMARIZECOLUMNS(
			'date_dim'[d_quarter_name],
			__DS0FilterTable,
			__DS0FilterTable2,
			__DS0FilterTable3,
			__DS0FilterTable4,
			__DS0FilterTable5,
			"Catalog_Sales_Quantity", 'Measures 1'[Catalog Sales Quantity],
			"Catalog_Sales_Same_Period_LY", 'Measures 1'[Catalog Sales Same Period LY],
			"Catalog_Sales_YoY", 'Measures 1'[Catalog Sales YoY]
		)

	VAR __DS0PrimaryWindowed = 
		TOPN(1001, __DS0Core, 'date_dim'[d_quarter_name], 0)

EVALUATE
	__DS0PrimaryWindowed

ORDER BY
	'date_dim'[d_quarter_name] DESC

## S3 Q4
// DAX Query
DEFINE
	VAR __DS0FilterTable = 
		TREATAS({"CA"}, 'customer_address'[ca_state])

	VAR __DS0FilterTable2 = 
		TREATAS({"College"}, 'customer_demographics'[cd_education_status])

	VAR __DS0FilterTable3 = 
		TREATAS({"Brett Yates"}, 'store'[s_manager])

	VAR __DS0FilterTable4 = 
		TREATAS({"DHL"}, 'ship_mode'[sm_carrier])

	VAR __DS0FilterTable5 = 
		TREATAS({"quarterly"}, 'catalog_page'[cp_type])

	VAR __DS0FilterTable6 = 
		TREATAS({"'date_dim'[d_quarter_name]"}, 'Time Unit'[Time Unit Fields])

	VAR __DS0FilterTable7 = 
		TREATAS({2026}, 'date_dim'[d_year])

	VAR __DS0FilterTable8 = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __DS0FilterTable9 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

	VAR __DS0Core = 
		SUMMARIZECOLUMNS(
			'date_dim'[d_quarter_name],
			__DS0FilterTable,
			__DS0FilterTable2,
			__DS0FilterTable3,
			__DS0FilterTable4,
			__DS0FilterTable5,
			__DS0FilterTable6,
			__DS0FilterTable7,
			__DS0FilterTable8,
			__DS0FilterTable9,
			"Catalog_Sales_Quantity", 'Measures 1'[Catalog Sales Quantity],
			"Catalog_Sales_Same_Period_LY", 'Measures 1'[Catalog Sales Same Period LY],
			"Catalog_Sales_YoY", 'Measures 1'[Catalog Sales YoY]
		)

	VAR __DS0PrimaryWindowed = 
		TOPN(1001, __DS0Core, 'date_dim'[d_quarter_name], 0)

EVALUATE
	__DS0PrimaryWindowed

ORDER BY
	'date_dim'[d_quarter_name] DESC


## S1 Q5
// DAX Query
DEFINE
	VAR __DS0FilterTable = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __DS0FilterTable2 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

	VAR __DS0Core = 
		SUMMARIZECOLUMNS(
			'item'[i_category],
			'date_dim'[d_year],
			'date_dim'[d_quarter_name],
			__DS0FilterTable,
			__DS0FilterTable2,
			"Store_Revenue", 'Measures 1'[Store Revenue],
			"Store_Revenue_YoY", 'Measures 1'[Store Revenue YoY],
			"Store_Revenue_YTD", 'Measures 1'[Store Revenue YTD]
		)

	VAR __DS0PrimaryWindowed = 
		TOPN(501, __DS0Core, 'item'[i_category], 0, 'date_dim'[d_year], 1, 'date_dim'[d_quarter_name], 1)

EVALUATE
	__DS0PrimaryWindowed

ORDER BY
	'item'[i_category] DESC, 'date_dim'[d_year], 'date_dim'[d_quarter_name]


## S2 Q5
// DAX Query
DEFINE
	VAR __DS0FilterTable = 
		TREATAS({"CO"}, 'customer_address'[ca_state])

	VAR __DS0FilterTable2 = 
		TREATAS({"Advanced Degree"}, 'customer_demographics'[cd_education_status])

	VAR __DS0FilterTable3 = 
		TREATAS({"'date_dim'[d_quarter_name]"}, 'Time Unit'[Time Unit Fields])

	VAR __DS0FilterTable4 = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __DS0FilterTable5 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

	VAR __DS0Core = 
		SUMMARIZECOLUMNS(
			'item'[i_category],
			'date_dim'[d_quarter_name],
			__DS0FilterTable,
			__DS0FilterTable2,
			__DS0FilterTable3,
			__DS0FilterTable4,
			__DS0FilterTable5,
			"Store_Revenue", 'Measures 1'[Store Revenue],
			"Store_Revenue_YoY", 'Measures 1'[Store Revenue YoY],
			"Store_Revenue_YTD", 'Measures 1'[Store Revenue YTD]
		)

	VAR __DS0PrimaryWindowed = 
		TOPN(501, __DS0Core, 'item'[i_category], 0, 'date_dim'[d_quarter_name], 1)

EVALUATE
	__DS0PrimaryWindowed

ORDER BY
	'item'[i_category] DESC, 'date_dim'[d_quarter_name]


## S3 Q5
// DAX Query
DEFINE
	VAR __DS0FilterTable = 
		TREATAS({"CA"}, 'customer_address'[ca_state])

	VAR __DS0FilterTable2 = 
		TREATAS({"College"}, 'customer_demographics'[cd_education_status])

	VAR __DS0FilterTable3 = 
		TREATAS({"Brett Yates"}, 'store'[s_manager])

	VAR __DS0FilterTable4 = 
		TREATAS({"DHL"}, 'ship_mode'[sm_carrier])

	VAR __DS0FilterTable5 = 
		TREATAS({"quarterly"}, 'catalog_page'[cp_type])

	VAR __DS0FilterTable6 = 
		TREATAS({"'date_dim'[d_quarter_name]"}, 'Time Unit'[Time Unit Fields])

	VAR __DS0FilterTable7 = 
		TREATAS({2026}, 'date_dim'[d_year])

	VAR __DS0FilterTable8 = 
		FILTER(
			KEEPFILTERS(VALUES('catalog_sales'[cache_buster])),
			'catalog_sales'[cache_buster] < 2
		)

	VAR __DS0FilterTable9 = 
		FILTER(KEEPFILTERS(VALUES('store_sales'[cache_buster])), 'store_sales'[cache_buster] < 2)

	VAR __DS0Core = 
		SUMMARIZECOLUMNS(
			'item'[i_category],
			'date_dim'[d_quarter_name],
			__DS0FilterTable,
			__DS0FilterTable2,
			__DS0FilterTable3,
			__DS0FilterTable4,
			__DS0FilterTable5,
			__DS0FilterTable6,
			__DS0FilterTable7,
			__DS0FilterTable8,
			__DS0FilterTable9,
			"Store_Revenue", 'Measures 1'[Store Revenue],
			"Store_Revenue_YoY", 'Measures 1'[Store Revenue YoY],
			"Store_Revenue_YTD", 'Measures 1'[Store Revenue YTD]
		)

	VAR __DS0PrimaryWindowed = 
		TOPN(501, __DS0Core, 'item'[i_category], 0, 'date_dim'[d_quarter_name], 1)

EVALUATE
	__DS0PrimaryWindowed

ORDER BY
	'item'[i_category] DESC, 'date_dim'[d_quarter_name]

