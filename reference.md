# Reference
## API Evm Dex
<details><summary><code>client.API.Evm.Dex.GetWalletProfile(request) -> *api.EvmDexWalletProfile</code></summary>
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
request := &evm.GetWalletProfileDexRequest{
        ChainID: 1,
        Wallet: "0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045",
        Options: &api.EvmDexWalletProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.EvmDexWalletProfileTimeWindowEnum{
                api.EvmDexWalletProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Evm.Dex.GetWalletProfile(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**wallet:** `string` — Wallet address to retrieve the profile for.
    
</dd>
</dl>

<dl>
<dd>

**options:** `*api.EvmDexWalletProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Evm.Dex.SearchWalletProfiles(request) -> *evm.SearchWalletProfilesDexResponse</code></summary>
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
request := &evm.SearchWalletProfilesDexRequest{
        Limit: prism.Int(
            10,
        ),
        ChainID: 1,
        Query: &api.EvmDexWalletProfileSearchPayloadQuery{
            Fields: []api.EvmDexWalletProfileSearchPayloadQueryTargetsEnum{
                api.EvmDexWalletProfileSearchPayloadQueryTargetsEnumWalletAddress,
            },
            Text: "0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045",
        },
        Sort: &api.EvmDexProfileSearchPayloadSort{
            Field: "metrics.7d.cumulative_pnl",
            Direction: api.EvmDexProfileSearchPayloadSortDirectionEnumDesc,
        },
        Options: &api.EvmDexWalletProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.EvmDexWalletProfileTimeWindowEnum{
                api.EvmDexWalletProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Evm.Dex.SearchWalletProfiles(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**query:** `*api.EvmDexWalletProfileSearchPayloadQuery` 
    
</dd>
</dl>

<dl>
<dd>

**filter:** `*api.EvmDexProfileSearchPayloadFilter` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*api.EvmDexProfileSearchPayloadSort` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `*api.EvmDexWalletProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Evm.Dex.GetTokenProfile(request) -> *api.EvmDexTokenProfile</code></summary>
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
request := &evm.GetTokenProfileDexRequest{
        ChainID: 1,
        Token: "0x6982508145454Ce325dDbE47a25d4ec3d2311933",
        Options: &api.EvmDexTokenProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.EvmDexTokenProfileTimeWindowEnum{
                api.EvmDexTokenProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Evm.Dex.GetTokenProfile(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**token:** `string` — Token address to retrieve the profile for.
    
</dd>
</dl>

<dl>
<dd>

**options:** `*api.EvmDexTokenProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Evm.Dex.SearchTokenProfiles(request) -> *evm.SearchTokenProfilesDexResponse</code></summary>
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
request := &evm.SearchTokenProfilesDexRequest{
        Limit: prism.Int(
            10,
        ),
        ChainID: 1,
        Query: &api.EvmDexTokenProfileSearchPayloadQueryField{
            Fields: []api.EvmDexTokenProfileSearchPayloadQueryFieldTargetsEnum{
                api.EvmDexTokenProfileSearchPayloadQueryFieldTargetsEnumTokenAddress,
            },
            Text: "0x6982508145454Ce325dDbE47a25d4ec3d2311933",
        },
        Sort: &api.EvmDexProfileSearchPayloadSort{
            Field: "metrics.1d.usd_volume",
            Direction: api.EvmDexProfileSearchPayloadSortDirectionEnumDesc,
        },
        Options: &api.EvmDexTokenProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.EvmDexTokenProfileTimeWindowEnum{
                api.EvmDexTokenProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Evm.Dex.SearchTokenProfiles(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**query:** `*api.EvmDexTokenProfileSearchPayloadQueryField` 
    
</dd>
</dl>

<dl>
<dd>

**filter:** `*api.EvmDexProfileSearchPayloadFilter` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*api.EvmDexProfileSearchPayloadSort` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `*api.EvmDexTokenProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Evm.Dex.GetPositionProfile(request) -> *api.EvmDexPositionProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a position profile for a specific wallet-token pair.
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
request := &evm.GetPositionProfileDexRequest{
        ChainID: 1,
        Wallet: "0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045",
        Token: "0x6982508145454Ce325dDbE47a25d4ec3d2311933",
        Options: &api.EvmDexPositionProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.EvmDexPositionProfileTimeWindowEnum{
                api.EvmDexPositionProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Evm.Dex.GetPositionProfile(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**wallet:** `string` — Wallet address of the position to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**token:** `string` — Token address of the position to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**options:** `*api.EvmDexPositionProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Evm.Dex.SearchPositionProfiles(request) -> *evm.SearchPositionProfilesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter, query, and sort position profiles based on specified metrics and conditions.
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
request := &evm.SearchPositionProfilesDexRequest{
        Limit: prism.Int(
            10,
        ),
        ChainID: 1,
        Sort: &api.EvmDexProfileSearchPayloadSort{
            Field: "metrics.7d.pnl",
            Direction: api.EvmDexProfileSearchPayloadSortDirectionEnumDesc,
        },
        Options: &api.EvmDexPositionProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.EvmDexPositionProfileTimeWindowEnum{
                api.EvmDexPositionProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Evm.Dex.SearchPositionProfiles(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**filter:** `*api.EvmDexProfileSearchPayloadFilter` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*api.EvmDexProfileSearchPayloadSort` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `*api.EvmDexPositionProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Evm.Dex.GetTrades(request) -> *evm.GetTradesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns trades for a wallet and/or token on a single chain.
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
request := &evm.GetTradesDexRequest{
        Limit: prism.Int(
            20,
        ),
        ChainID: 1,
        Wallet: prism.String(
            "0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045",
        ),
    }
client.API.Evm.Dex.GetTrades(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**wallet:** `*string` — Wallet address to filter trades by.
    
</dd>
</dl>

<dl>
<dd>

**token:** `*string` — Token address to filter trades by.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Evm.Dex.GetSwaps(request) -> *evm.GetSwapsDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns swaps for a combination of wallet, token and/or pool.
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
request := &evm.GetSwapsDexRequest{
        Limit: prism.Int(
            20,
        ),
        ChainID: 1,
        Wallet: prism.String(
            "0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045",
        ),
    }
client.API.Evm.Dex.GetSwaps(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**wallet:** `*string` — Wallet address to filter swaps by.
    
</dd>
</dl>

<dl>
<dd>

**token:** `*string` — Token address to filter swaps by.
    
</dd>
</dl>

<dl>
<dd>

**pool:** `*string` — Pool address to filter swaps by.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Evm.Dex.GetPrice(request) -> []*api.EvmDexPrice</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns prices for one or more tokens or pools.
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
request := &evm.GetPriceDexRequest{
        ChainID: 1,
        Tokens: []string{
            "0x6982508145454Ce325dDbE47a25d4ec3d2311933",
        },
    }
client.API.Evm.Dex.GetPrice(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**tokens:** `[]string` — Token addresses to retrieve the latest prices for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `[]string` — Pool addresses to retrieve the latest prices for.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Evm.Dex.GetPriceStats(request) -> []*api.EvmDexPriceStats</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price stats for one or more tokens or pools.
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
request := &evm.GetPriceStatsDexRequest{
        ChainID: 1,
        Tokens: []string{
            "0x6982508145454Ce325dDbE47a25d4ec3d2311933",
        },
    }
client.API.Evm.Dex.GetPriceStats(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**tokens:** `[]string` — Token addresses to retrieve price statistics for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `[]string` — Pool addresses to retrieve price statistics for.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Evm.Dex.GetPriceCandles(request) -> []*api.EvmDexPriceCandle</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price candles for a specific token and/or pool.
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
request := &evm.GetPriceCandlesDexRequest{
        ChainID: 1,
        Token: prism.String(
            "0x6982508145454Ce325dDbE47a25d4ec3d2311933",
        ),
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
client.API.Evm.Dex.GetPriceCandles(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**token:** `*string` — Token address to filter by.
    
</dd>
</dl>

<dl>
<dd>

**pool:** `*string` — Pool address to filter by.
    
</dd>
</dl>

<dl>
<dd>

**from:** `*time.Time` 

Start of the candle range, as a date-time RFC3339 string.
Can be combined with `to` to define a bounded range.
    
</dd>
</dl>

<dl>
<dd>

**to:** `*time.Time` 

End of the candle range, as a date-time RFC3339 string. 
Defaults to the current time.
    
</dd>
</dl>

<dl>
<dd>

**count:** `*int` 

Number of candles to return.
Must be combined with `from` or `to`.
    
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

<details><summary><code>client.API.Evm.Dex.GetPriceHistory(request) -> []*api.EvmDexPriceHistory</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price history for one or more tokens or pools.
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
request := &evm.GetPriceHistoryDexRequest{
        ChainID: 1,
        Tokens: []string{
            "0x6982508145454Ce325dDbE47a25d4ec3d2311933",
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
client.API.Evm.Dex.GetPriceHistory(
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

**chainID:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**tokens:** `[]string` — Token addresses to retrieve price history for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `[]string` — Pool addresses to retrieve price history for.
    
</dd>
</dl>

<dl>
<dd>

**from:** `time.Time` — Start of the history range, as a date-time RFC3339 string.
    
</dd>
</dl>

<dl>
<dd>

**to:** `*time.Time` 

End of the history range, as a date-time RFC3339 string. 
Defaults to the current time.
    
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
            Fields: []api.SolanaDexWalletProfileSearchPayloadQueryTargetsEnum{
                api.SolanaDexWalletProfileSearchPayloadQueryTargetsEnumIdentityName,
            },
            Text: "cupsey",
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
            Fields: []api.SolanaDexTokenProfileSearchPayloadQueryFieldTargetsEnum{
                api.SolanaDexTokenProfileSearchPayloadQueryFieldTargetsEnumMetadataName,
            },
            Text: "bonk",
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

<details><summary><code>client.API.Solana.Dex.GetPositionProfile(request) -> *api.SolanaDexPositionProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a position profile for a specific wallet-token pair.
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
request := &solana.GetPositionProfileDexRequest{
        Wallet: "suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
        Token: "Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk",
        Options: &api.SolanaDexPositionProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeLabels: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.SolanaDexPositionProfileTimeWindowEnum{
                api.SolanaDexPositionProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Solana.Dex.GetPositionProfile(
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

**wallet:** `string` — Wallet address of the position to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**token:** `string` — Token address of the position to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**options:** `*api.SolanaDexPositionProfilePayloadOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.API.Solana.Dex.SearchPositionProfiles(request) -> *solana.SearchPositionProfilesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter, query, and sort position profiles based on specified metrics and conditions.
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
request := &solana.SearchPositionProfilesDexRequest{
        Limit: prism.Int(
            10,
        ),
        Sort: &api.SolanaDexProfileSearchPayloadSort{
            Field: "metrics.7d.pnl",
            Direction: api.SolanaDexProfileSearchPayloadSortDirectionEnumDesc,
        },
        DynamicLabels: &api.SolanaDexProfileSearchPayloadDynamicLabels{
            "winner": &api.SolanaDexProfileSearchPayloadFilter{},
        },
        Options: &api.SolanaDexPositionProfilePayloadOptions{
            IncludeMetadata: prism.Bool(
                true,
            ),
            IncludeLabels: prism.Bool(
                true,
            ),
            IncludeMetrics: []api.SolanaDexPositionProfileTimeWindowEnum{
                api.SolanaDexPositionProfileTimeWindowEnumWindow7D,
            },
        },
    }
client.API.Solana.Dex.SearchPositionProfiles(
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

**options:** `*api.SolanaDexPositionProfilePayloadOptions` 
    
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

Returns trades for a combination of wallet, token and/or pool.
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

**wallet:** `*string` — Wallet address to filter trades by.
    
</dd>
</dl>

<dl>
<dd>

**token:** `*string` — Token address to filter trades by.
    
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

Returns swaps for a combination of wallet, token and/or pool.
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

**wallet:** `*string` — Wallet address to filter swaps by.
    
</dd>
</dl>

<dl>
<dd>

**token:** `*string` — Token address to filter swaps by.
    
</dd>
</dl>

<dl>
<dd>

**pool:** `*string` — Pool address to filter swaps by.
    
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

Returns prices for one or more tokens or pools.
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

**tokens:** `[]string` — Token addresses to retrieve the latest prices for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `[]string` — Pool addresses to retrieve the latest prices for.
    
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

Returns price stats for one or more tokens or pools.
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

**tokens:** `[]string` — Token addresses to retrieve price statistics for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `[]string` — Pool addresses to retrieve price statistics for.
    
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

Returns price candles for a specific token and/or pool.
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
        Token: prism.String(
            "Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk",
        ),
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

**token:** `*string` — Token address to filter by.
    
</dd>
</dl>

<dl>
<dd>

**pool:** `*string` — Pool address to filter by.
    
</dd>
</dl>

<dl>
<dd>

**from:** `*time.Time` 

Start of the candle range, as a date-time RFC3339 string.
Can be combined with `to` to define a bounded range.
    
</dd>
</dl>

<dl>
<dd>

**to:** `*time.Time` 

End of the candle range, as a date-time RFC3339 string. 
Defaults to the current time.
    
</dd>
</dl>

<dl>
<dd>

**count:** `*int` 

Number of candles to return.
Must be combined with `from` or `to`.
    
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

Returns price history for one or more tokens or pools.
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

**tokens:** `[]string` — Token addresses to retrieve price history for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `[]string` — Pool addresses to retrieve price history for.
    
</dd>
</dl>

<dl>
<dd>

**from:** `time.Time` — Start of the history range, as a date-time RFC3339 string.
    
</dd>
</dl>

<dl>
<dd>

**to:** `*time.Time` 

End of the history range, as a date-time RFC3339 string. 
Defaults to the current time.
    
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

