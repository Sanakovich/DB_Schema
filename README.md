USE [DB_TEST]
GO
/****** Object:  Table [dbo].[Oders_Details_tbl]    Script Date: 11/01/2021 15:55:02 ******/
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE [dbo].[Oders_Details_tbl](
	[BL_Details_ID] [int] NOT NULL,
	[BLID] [int] NOT NULL,
	[Prd_Name] [nvarchar](80) NULL,
	[Qty_Interior] [int] NULL,
	[Unit_Price] [decimal](20, 2) NULL,
	[Box_Price] [decimal](20, 2) NULL,
	[QuantitY] [int] NULL,
	[Total_Price] [decimal](20, 2) NULL,
 CONSTRAINT [PK_Oders_Details] PRIMARY KEY CLUSTERED 
(
	[BL_Details_ID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]

GO
/****** Object:  Table [dbo].[Orders_tbl]    Script Date: 11/01/2021 15:55:02 ******/
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE [dbo].[Orders_tbl](
	[BLID] [int] NOT NULL,
	[DateTime] [smalldatetime] NULL,
	[ClientFullName] [nvarchar](50) NULL,
	[ClientPhone] [nvarchar](50) NULL,
	[Total_Products] [int] NULL,
	[Total_Quantity] [int] NULL,
	[Total_Amount] [decimal](20, 2) NULL,
	[Received] [decimal](20, 2) NULL,
	[Rest] [decimal](20, 2) NULL,
	[Discount] [decimal](20, 2) NULL,
	[State] [bit] NULL,
	[RealizedBy] [nvarchar](50) NULL,
 CONSTRAINT [PK_Orders] PRIMARY KEY CLUSTERED 
(
	[BLID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]

GO
/****** Object:  Table [dbo].[Products_tbl]    Script Date: 11/01/2021 15:55:02 ******/
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE [dbo].[Products_tbl](
	[Prd_ID] [int] NOT NULL,
	[Prd_Name] [nvarchar](80) NULL,
	[Prd_Category] [nvarchar](50) NULL,
	[Qty_Available] [int] NULL,
	[Qty_Minimal] [int] NULL,
	[Qty_Interior] [int] NULL,
	[Cost_Price] [decimal](19, 2) NULL,
	[Sell_Price] [decimal](19, 2) NULL,
	[Second_Price] [decimal](19, 2) NULL,
	[Minimal_Price] [decimal](19, 2) NULL,
	[Profit] [decimal](19, 2) NULL,
	[Expiration_Date] [date] NULL,
	[Enabled] [bit] NULL,
 CONSTRAINT [PK_Products_tbl] PRIMARY KEY CLUSTERED 
(
	[Prd_ID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]

GO
/****** Object:  Table [dbo].[Users_tbl]    Script Date: 11/01/2021 15:55:02 ******/
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE [dbo].[Users_tbl](
	[ID] [int] NOT NULL,
	[UserFullName] [nvarchar](80) NULL,
	[PhoneNumber] [nvarchar](80) NULL,
	[UserName] [nvarchar](50) NULL,
	[UserPassword] [nvarchar](50) NULL,
	[BuysManagment] [bit] NULL,
	[SuppliersManagment] [bit] NULL,
	[SellsManagment] [bit] NULL,
	[ClientsManagment] [bit] NULL,
	[StockManagment] [bit] NULL,
	[Settings] [bit] NULL,
	[Administrator] [bit] NULL,
	[DateAdded] [datetime] NULL,
	[AddedBy] [nvarchar](80) NULL,
 CONSTRAINT [PK_Users_tbl] PRIMARY KEY CLUSTERED 
(
	[ID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]

GO
