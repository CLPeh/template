# Unit Testing

<details><summary> GetPromotionTransaction </summary>

General Test Data:
```sh
PlayerId = 1146580829,
PlayerName = "zhihaochan",
PromotionId = 556,
OperatorIds = new List<uint> { 1 },
OperatorTokens = new List<string> { `operatorTokens` },
CallerOperatorId = 1,
CallerOperatorToken = "abcd",
PageNumber = 1,
RowCount = 25,
ServiceType = `serviceType`,
```

Valid Test Data:
```sh
serviceType = ServiceType.External
operatorTokens = null

serviceType = ServiceType.BackOffice
operatorTokens = "abcd"

serviceType = ServiceType.GameProxy
operatorTokens = "abcd"
```

Invalid Test Data:
```sh
serviceType = ServiceType.External
operatorTokens = "123!@#"

serviceType = ServiceType.BackOffice
operatorTokens = "123!@#"

serviceType = ServiceType.GameProxy
operatorTokens = "123!@#"
```

</details>

<details><summary> GetPromotionTransactionSummary </summary>

General Test Data:
```sh
StartTime = new DateTime(2023, 01, 01),
EndTime = new DateTime(2023, 04, 30),
PromotionId = 419,
Currency = "CNY",
OperatorIds = new List<uint> { operaterId },
OperatorTokens = new List<string> { operatorTokens },
CallerOperatorId = 1,
CallerOperatorToken = "abcd",
PageNumber = 1,
RowCount = 15,
OrderBy = "player_id",
SortBy = (int)Sorting.Ascending,
ServiceType = serviceType,
```

Valid Test Data:
```sh
serviceType = ServiceType.External
- operatorTokens = null, operatorId = 0

serviceType = ServiceType.BackOffice
- operatorTokens = null, operatorId = 0
- operatorTokens = "abcd", operatorId = 1
```

Invalid Test Data:
```sh
serviceType = ServiceType.External
operatorTokens = "123!@#"

serviceType = ServiceType.BackOffice
operatorTokens = "123!@#"
```

</details>

