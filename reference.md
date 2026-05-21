# Reference
## API Solana Dex
<details><summary><code>client.API.Solana.Dex.GetWalletProfile(request) -> *api.SolanaDexWalletProfile</code></summary>
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
        Options: &api.SolanaDexWalletProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeLabels: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.SolanaDexWalletProfileTimeWindowEnum{
                api.SolanaDexWalletProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Solana.Dex.GetWalletProfile(
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

**options:** `*api.SolanaDexWalletProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Solana.Dex.SearchWalletProfiles(request) -> *solana.SearchWalletProfilesDexResponse</code></summary>
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
        Limit: prism.Int(
            10,
        ),
        Query: &api.SolanaDexWalletProfileSearchPayloadQuery{
            Text: "cupsey",
            Fields: []api.SolanaDexWalletProfileSearchPayloadQueryTargetsEnum{
                api.SolanaDexWalletProfileSearchPayloadQueryTargetsEnumIdentityName,
            },
        },
        Sort: &api.SolanaDexProfileSearchPayloadSort{
            Field: "metrics.7d.cumulative_pnl",
            Direction: api.SolanaDexProfileSearchPayloadSortDirectionEnumDesc,
        },
        DynamicLabels: &api.SolanaDexProfileSearchPayloadDynamicLabels{
            "smart": &api.SolanaDexProfileSearchPayloadFilter{},
        },
        Options: &api.SolanaDexWalletProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeLabels: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.SolanaDexWalletProfileTimeWindowEnum{
                api.SolanaDexWalletProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Solana.Dex.SearchWalletProfiles(
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

**query:** `*api.SolanaDexWalletProfileSearchPayloadQuery` 
    
</dd>
</dl>

<dl>
<dd>

**filter:** `*api.SolanaDexProfileSearchPayloadFilter` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*api.SolanaDexProfileSearchPayloadSort` 
    
</dd>
</dl>

<dl>
<dd>

**dynamicLabels:** `*api.SolanaDexProfileSearchPayloadDynamicLabels` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `*api.SolanaDexWalletProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Solana.Dex.GetTokenProfile(request) -> *api.SolanaDexTokenProfile</code></summary>
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
        Options: &api.SolanaDexTokenProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeMarket: prism.Bool(
                true,
            ),
            IncludeLabels: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.SolanaDexTokenProfileTimeWindowEnum{
                api.SolanaDexTokenProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Solana.Dex.GetTokenProfile(
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

**options:** `*api.SolanaDexTokenProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Solana.Dex.SearchTokenProfiles(request) -> *solana.SearchTokenProfilesDexResponse</code></summary>
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
        Limit: prism.Int(
            10,
        ),
        Query: &api.SolanaDexTokenProfileSearchPayloadQueryField{
            Text: "bonk",
            Fields: []api.SolanaDexTokenProfileSearchPayloadQueryFieldTargetsEnum{
                api.SolanaDexTokenProfileSearchPayloadQueryFieldTargetsEnumMetadataName,
            },
        },
        Sort: &api.SolanaDexProfileSearchPayloadSort{
            Field: "market.liquidity",
            Direction: api.SolanaDexProfileSearchPayloadSortDirectionEnumDesc,
        },
        DynamicLabels: &api.SolanaDexProfileSearchPayloadDynamicLabels{
            "trending": &api.SolanaDexProfileSearchPayloadFilter{},
        },
        Options: &api.SolanaDexTokenProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeMarket: prism.Bool(
                true,
            ),
            IncludeLabels: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.SolanaDexTokenProfileTimeWindowEnum{
                api.SolanaDexTokenProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Solana.Dex.SearchTokenProfiles(
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

**query:** `*api.SolanaDexTokenProfileSearchPayloadQueryField` 
    
</dd>
</dl>

<dl>
<dd>

**filter:** `*api.SolanaDexProfileSearchPayloadFilter` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*api.SolanaDexProfileSearchPayloadSort` 
    
</dd>
</dl>

<dl>
<dd>

**dynamicLabels:** `*api.SolanaDexProfileSearchPayloadDynamicLabels` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `*api.SolanaDexTokenProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Solana.Dex.GetTrades(request) -> *solana.GetTradesDexResponse</code></summary>
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
        Limit: prism.Int(
            20,
        ),
        Wallet: prism.String(
            "suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
        ),
    }
client.API.Solana.Dex.GetTrades(
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

<details><summary><code>client.API.Solana.Dex.GetSwaps(request) -> *solana.GetSwapsDexResponse</code></summary>
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
        Limit: prism.Int(
            20,
        ),
        Wallet: prism.String(
            "suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
        ),
    }
client.API.Solana.Dex.GetSwaps(
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

<details><summary><code>client.API.Solana.Dex.GetPrice(request) -> []*api.SolanaDexPrice</code></summary>
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
client.API.Solana.Dex.GetPrice(
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

<details><summary><code>client.API.Solana.Dex.GetPriceStats(request) -> []*api.SolanaDexPriceStats</code></summary>
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
client.API.Solana.Dex.GetPriceStats(
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

<details><summary><code>client.API.Solana.Dex.GetPriceCandles(request) -> []*api.SolanaDexPriceCandle</code></summary>
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
        From: prism.Time(
            prism.MustParseDateTime(
                "2026-04-27T00:00:00Z",
            ),
        ),
        To: prism.Time(
            prism.MustParseDateTime(
                "2026-04-27T01:00:00Z",
            ),
        ),
        Interval: 60,
    }
client.API.Solana.Dex.GetPriceCandles(
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

<details><summary><code>client.API.Solana.Dex.GetPriceHistory(request) -> []*api.SolanaDexPriceHistory</code></summary>
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
        From: prism.MustParseDateTime(
            "2026-04-27T00:00:00Z",
        ),
        To: prism.Time(
            prism.MustParseDateTime(
                "2026-04-27T01:00:00Z",
            ),
        ),
        Interval: 3600,
    }
client.API.Solana.Dex.GetPriceHistory(
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

