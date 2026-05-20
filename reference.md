# Reference
## Solana Dex
<details><summary><code>client.Solana.Dex.GetWalletProfile(request) -> *sdkgo.SolanaDexWalletProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a wallet profile for a specific wallet.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &solana.GetWalletProfileDexRequest{
        Wallet: "suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
        Options: &sdkgo.SolanaDexWalletProfilePayloadOptions{
            IncludeMetadata: sdkgo.Bool(
                true,
            ),
            IncludeLabels: sdkgo.Bool(
                true,
            ),
            IncludeMetrics: []sdkgo.SolanaDexWalletProfileTimeWindowEnum{
                sdkgo.SolanaDexWalletProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.Solana.Dex.GetWalletProfile(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**wallet:** `string` — Wallet address to retrieve the profile for.
    
</dd>
</dl>

<dl>
<dd>

**options:** `*sdkgo.SolanaDexWalletProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Solana.Dex.SearchWalletProfiles(request) -> *solana.SearchWalletProfilesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter, query, and sort wallet profiles based on specified metrics and conditions.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &solana.SearchWalletProfilesDexRequest{
        Limit: sdkgo.Int(
            10,
        ),
        Query: &sdkgo.SolanaDexWalletProfileSearchPayloadQuery{
            Text: "cupsey",
            Fields: []sdkgo.SolanaDexWalletProfileSearchPayloadQueryTargetsEnum{
                sdkgo.SolanaDexWalletProfileSearchPayloadQueryTargetsEnumWalletAddress,
            },
        },
        Sort: &sdkgo.SolanaDexProfileSearchPayloadSort{
            Field: "metrics.7d.cumulative_pnl",
            Direction: sdkgo.SolanaDexProfileSearchPayloadSortDirectionEnumDesc,
        },
        DynamicLabels: &sdkgo.SolanaDexProfileSearchPayloadDynamicLabels{
            "smart": &sdkgo.SolanaDexProfileSearchPayloadFilter{},
        },
        Options: &sdkgo.SolanaDexWalletProfilePayloadOptions{
            IncludeMetadata: sdkgo.Bool(
                true,
            ),
            IncludeLabels: sdkgo.Bool(
                true,
            ),
            IncludeMetrics: []sdkgo.SolanaDexWalletProfileTimeWindowEnum{
                sdkgo.SolanaDexWalletProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.Solana.Dex.SearchWalletProfiles(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**query:** `*sdkgo.SolanaDexWalletProfileSearchPayloadQuery` 
    
</dd>
</dl>

<dl>
<dd>

**filter:** `*sdkgo.SolanaDexProfileSearchPayloadFilter` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*sdkgo.SolanaDexProfileSearchPayloadSort` 
    
</dd>
</dl>

<dl>
<dd>

**dynamicLabels:** `*sdkgo.SolanaDexProfileSearchPayloadDynamicLabels` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `*sdkgo.SolanaDexWalletProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Solana.Dex.GetTokenProfile(request) -> *sdkgo.SolanaDexTokenProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the profile for a specific token.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &solana.GetTokenProfileDexRequest{
        Token: "Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk",
        Options: &sdkgo.SolanaDexTokenProfilePayloadOptions{
            IncludeMetadata: sdkgo.Bool(
                true,
            ),
            IncludeMarket: sdkgo.Bool(
                true,
            ),
            IncludeLabels: sdkgo.Bool(
                true,
            ),
            IncludeMetrics: []sdkgo.SolanaDexTokenProfileTimeWindowEnum{
                sdkgo.SolanaDexTokenProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.Solana.Dex.GetTokenProfile(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**token:** `string` — Token address to retrieve the profile for.
    
</dd>
</dl>

<dl>
<dd>

**options:** `*sdkgo.SolanaDexTokenProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Solana.Dex.SearchTokenProfiles(request) -> *solana.SearchTokenProfilesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter, query, and sort token profiles based on specified metrics and conditions.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &solana.SearchTokenProfilesDexRequest{
        Limit: sdkgo.Int(
            10,
        ),
        Query: &sdkgo.SolanaDexTokenProfileSearchPayloadQueryField{
            Text: "bonk",
            Fields: []sdkgo.SolanaDexTokenProfileSearchPayloadQueryFieldTargetsEnum{
                sdkgo.SolanaDexTokenProfileSearchPayloadQueryFieldTargetsEnumMetadataName,
            },
        },
        Sort: &sdkgo.SolanaDexProfileSearchPayloadSort{
            Field: "market.liquidity",
            Direction: sdkgo.SolanaDexProfileSearchPayloadSortDirectionEnumDesc,
        },
        DynamicLabels: &sdkgo.SolanaDexProfileSearchPayloadDynamicLabels{
            "trending": &sdkgo.SolanaDexProfileSearchPayloadFilter{},
        },
        Options: &sdkgo.SolanaDexTokenProfilePayloadOptions{
            IncludeMetadata: sdkgo.Bool(
                true,
            ),
            IncludeMarket: sdkgo.Bool(
                true,
            ),
            IncludeLabels: sdkgo.Bool(
                true,
            ),
            IncludeMetrics: []sdkgo.SolanaDexTokenProfileTimeWindowEnum{
                sdkgo.SolanaDexTokenProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.Solana.Dex.SearchTokenProfiles(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**query:** `*sdkgo.SolanaDexTokenProfileSearchPayloadQueryField` 
    
</dd>
</dl>

<dl>
<dd>

**filter:** `*sdkgo.SolanaDexProfileSearchPayloadFilter` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*sdkgo.SolanaDexProfileSearchPayloadSort` 
    
</dd>
</dl>

<dl>
<dd>

**dynamicLabels:** `*sdkgo.SolanaDexProfileSearchPayloadDynamicLabels` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `*sdkgo.SolanaDexTokenProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Solana.Dex.GetTrades(request) -> *solana.GetTradesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns trades for a wallet, token or both.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &solana.GetTradesDexRequest{
        Limit: sdkgo.Int(
            20,
        ),
        Wallet: sdkgo.String(
            "suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
        ),
    }
client.Solana.Dex.GetTrades(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**wallet:** `*string` — Wallet address to filter trades by. When combined with `token`, returns only trades for that wallet on that token.
    
</dd>
</dl>

<dl>
<dd>

**token:** `*string` — Token address to filter trades by. When combined with `wallet`, returns only trades for that wallet on that token.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Solana.Dex.GetSwaps(request) -> *solana.GetSwapsDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns swaps for a wallet, token or both.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &solana.GetSwapsDexRequest{
        Limit: sdkgo.Int(
            20,
        ),
        Wallet: sdkgo.String(
            "suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
        ),
    }
client.Solana.Dex.GetSwaps(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**wallet:** `*string` — Wallet address to filter swaps by. When combined with `token`, returns only swaps for that wallet on that token.
    
</dd>
</dl>

<dl>
<dd>

**token:** `*string` — Token address to filter swaps by. When combined with `wallet`, returns only swaps for that wallet on that token.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Solana.Dex.GetPrice(request) -> []*sdkgo.SolanaDexPrice</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns prices for one or more tokens.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &solana.GetPriceDexRequest{
        Tokens: []string{
            "Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk",
        },
    }
client.Solana.Dex.GetPrice(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tokens:** `[]string` — Token addresses to retrieve the latest prices for. Accepts between 1 and 1000 tokens per request.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Solana.Dex.GetPriceStats(request) -> []*sdkgo.SolanaDexPriceStats</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price stats for one or more tokens.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &solana.GetPriceStatsDexRequest{
        Tokens: []string{
            "Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk",
        },
    }
client.Solana.Dex.GetPriceStats(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tokens:** `[]string` — Token addresses to retrieve price statistics for. Accepts between 1 and 1000 tokens per request.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Solana.Dex.GetPriceCandles(request) -> []*sdkgo.SolanaDexPriceCandle</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price candles for a specific token.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &solana.GetPriceCandlesDexRequest{
        Token: "Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk",
        From: sdkgo.Time(
            sdkgo.MustParseDateTime(
                "2026-04-27T00:00:00Z",
            ),
        ),
        To: sdkgo.Time(
            sdkgo.MustParseDateTime(
                "2026-04-27T01:00:00Z",
            ),
        ),
        Interval: 60,
    }
client.Solana.Dex.GetPriceCandles(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**token:** `string` — Token address to retrieve price candles for.
    
</dd>
</dl>

<dl>
<dd>

**from:** `*time.Time` 

Start of the candle range, as a date-time RFC3339 string.
Must be combined with `to` to define a bounded range.
    
</dd>
</dl>

<dl>
<dd>

**to:** `*time.Time` 

End of the candle range, as a date-time RFC3339 string. Defaults to the current time.
Must be combined with either `from` (to define a bounded range) or `count` (to return the N most recent candles ending at `to`).
    
</dd>
</dl>

<dl>
<dd>

**count:** `*int` 

Number of candles to return, ending at `to`.
Must be combined with `to`.
    
</dd>
</dl>

<dl>
<dd>

**interval:** `int` — Sampling interval between data points, in seconds.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Solana.Dex.GetPriceHistory(request) -> []*sdkgo.SolanaDexPriceHistory</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price history for one or more tokens.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &solana.GetPriceHistoryDexRequest{
        Tokens: []string{
            "Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk",
        },
        From: sdkgo.MustParseDateTime(
            "2026-04-27T00:00:00Z",
        ),
        To: sdkgo.Time(
            sdkgo.MustParseDateTime(
                "2026-04-27T01:00:00Z",
            ),
        ),
        Interval: 3600,
    }
client.Solana.Dex.GetPriceHistory(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tokens:** `[]string` — Token addresses to retrieve price history for. Accepts between 1 and 100 tokens per request.
    
</dd>
</dl>

<dl>
<dd>

**from:** `time.Time` — Start of the history range, as a date-time RFC3339 string.
    
</dd>
</dl>

<dl>
<dd>

**to:** `*time.Time` — End of the history range, as a date-time RFC3339 string. Defaults to the current time.
    
</dd>
</dl>

<dl>
<dd>

**interval:** `int` — Sampling interval between data points, in seconds.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

