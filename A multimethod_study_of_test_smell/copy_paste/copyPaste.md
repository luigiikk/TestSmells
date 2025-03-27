## Copy-Paste (Go)

```golang
  case bbtProto.CollectionType_SELF_PICKUP:
    q = fmt.Sprintf(
        "upad:t=%d_uid=%s_bid=%s_type=self_pickup:%s",
        alignedT,
        fmt.Sprint(CFG.Buyer.UserId),
        fmt.Sprint(CFG.BbtMap[bbtDataKey].BbtId),
        fmt.Sprint(CFG.BbtMap[bbtDataKey].ItemId))
  case bbtProto.CollectionType_DELIVERY:
    q = fmt.Sprintf(
        "upad:t=%d_uid=%s_bid=%s_type=self_pickup:%s",
        alignedT,
        fmt.Sprint(CFG.Buyer.UserId),
        fmt.Sprint(CFG.BbtMap[bbtDataKey].BbtId),
        fmt.Sprint(CFG.BbtMap[bbtDataKey].ItemId))
