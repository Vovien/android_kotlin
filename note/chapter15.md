## 功能需求及技术可行性分析

- 可以搜搜全球大多数国家的各个城市数据
- 可以查看全球绝大多数城市的天气信息
- 可以自由地切换城市，查看其他城市的天气
- 可以手动刷新实时的天气

使用彩云天气的 API 。

```
https://api.caiyunapp.com/v2/place?query=北京&token={token}&lang=zh_CN
https://api.caiyunapp.com/v2.5/{token}/116.353063,39.944876/realtime.json
https://api.caiyunapp.com/v2.5/{token}/116.353063,39.944876/daily.json
```

```json
{
    "status": "ok",
    "query": "北京",
    "places": [
        {
            "id": "6e8861ded5d03c5fdfe7a56526af08ecb433a575",
            "location": {
                "lat": 39.9041999,
                "lng": 116.4073963
            },
            "place_id": "g-6e8861ded5d03c5fdfe7a56526af08ecb433a575",
            "name": "北京市",
            "formatted_address": "中国北京市"
        },
        {
            "id": "B000A83C36",
            "name": "北京站",
            "formatted_address": "中国 北京市 东城区 毛家湾胡同甲13号",
            "location": {
                "lat": 39.902779,
                "lng": 116.427694
            },
            "place_id": "a-B000A83C36"
        },
        {
            "id": "B000A83M61",
            "name": "北京西站",
            "formatted_address": "中国 北京市 丰台区 莲花池东路118号",
            "location": {
                "lat": 39.89491,
                "lng": 116.322056
            },
            "place_id": "a-B000A83M61"
        },
        {
            "id": "B000A350CB",
            "name": "北京东站",
            "formatted_address": "中国 北京市 朝阳区 百子湾路7号",
            "location": {
                "lat": 39.90242,
                "lng": 116.485079
            },
            "place_id": "a-B000A350CB"
        },
        {
            "id": "B000A833V8",
            "name": "北京北站",
            "formatted_address": "中国 北京市 西城区 北滨河路1号",
            "location": {
                "lat": 39.944876,
                "lng": 116.353063
            },
            "place_id": "a-B000A833V8"
        }
    ]
}
```

```json
{
    "status": "ok",
    "api_version": "v2.5",
    "api_status": "active",
    "lang": "zh_CN",
    "unit": "metric",
    "tzshift": 28800,
    "timezone": "Asia/Shanghai",
    "server_time": 1588044624,
    "location": [
        39.944876,
        116.353063
    ],
    "result": {
        "realtime": {
            "status": "ok",
            "temperature": 22.79,
            "humidity": 0.31,
            "cloudrate": 0,
            "skycon": "CLEAR_DAY",
            "visibility": 9.8,
            "dswrf": 730,
            "wind": {
                "speed": 12.24,
                "direction": 173
            },
            "pressure": 100652.86,
            "apparent_temperature": 20.5,
            "precipitation": {
                "local": {
                    "status": "ok",
                    "datasource": "radar",
                    "intensity": 0
                },
                "nearest": {
                    "status": "ok",
                    "distance": 10000,
                    "intensity": 0
                }
            },
            "air_quality": {
                "pm25": 67,
                "pm10": 89,
                "o3": 158,
                "so2": 5,
                "no2": 51,
                "co": 0.7,
                "aqi": {
                    "chn": 90,
                    "usa": 157
                },
                "description": {
                    "chn": "良",
                    "usa": "中度污染"
                }
            },
            "life_index": {
                "ultraviolet": {
                    "index": 10,
                    "desc": "很强"
                },
                "comfort": {
                    "index": 5,
                    "desc": "舒适"
                }
            }
        },
        "primary": 0
    }
}
```

```json
{
    "status": "ok",
    "api_version": "v2.5",
    "api_status": "active",
    "lang": "zh_CN",
    "unit": "metric",
    "tzshift": 28800,
    "timezone": "Asia/Shanghai",
    "server_time": 1588044690,
    "location": [
        39.944876,
        116.353063
    ],
    "result": {
        "daily": {
            "status": "ok",
            "astro": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "sunrise": {
                        "time": "05:18"
                    },
                    "sunset": {
                        "time": "19:06"
                    }
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "sunrise": {
                        "time": "05:16"
                    },
                    "sunset": {
                        "time": "19:07"
                    }
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "sunrise": {
                        "time": "05:15"
                    },
                    "sunset": {
                        "time": "19:08"
                    }
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "sunrise": {
                        "time": "05:14"
                    },
                    "sunset": {
                        "time": "19:09"
                    }
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "sunrise": {
                        "time": "05:13"
                    },
                    "sunset": {
                        "time": "19:10"
                    }
                }
            ],
            "precipitation": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "max": 0,
                    "min": 0,
                    "avg": 0
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "max": 0,
                    "min": 0,
                    "avg": 0
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "max": 0,
                    "min": 0,
                    "avg": 0
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "max": 0,
                    "min": 0,
                    "avg": 0
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "max": 0.3245,
                    "min": 0,
                    "avg": 0.0223
                }
            ],
            "temperature": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "max": 30,
                    "min": 12,
                    "avg": 25.84
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "max": 32,
                    "min": 17,
                    "avg": 24.61
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "max": 31,
                    "min": 14,
                    "avg": 23.46
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "max": 32,
                    "min": 19,
                    "avg": 26.16
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "max": 33,
                    "min": 21,
                    "avg": 27.67
                }
            ],
            "wind": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "max": {
                        "speed": 24.7,
                        "direction": 207.45
                    },
                    "min": {
                        "speed": 0.21,
                        "direction": 72.6
                    },
                    "avg": {
                        "speed": 9.16,
                        "direction": 206.22
                    }
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "max": {
                        "speed": 23.98,
                        "direction": 209.53
                    },
                    "min": {
                        "speed": 4.26,
                        "direction": 206.95
                    },
                    "avg": {
                        "speed": 13.9,
                        "direction": 208.42
                    }
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "max": {
                        "speed": 18.88,
                        "direction": 211.21
                    },
                    "min": {
                        "speed": 1.3,
                        "direction": 311.89
                    },
                    "avg": {
                        "speed": 9.11,
                        "direction": 208.56
                    }
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "max": {
                        "speed": 17.99,
                        "direction": 207.74
                    },
                    "min": {
                        "speed": 0.5,
                        "direction": 278.72
                    },
                    "avg": {
                        "speed": 8.55,
                        "direction": 193.83
                    }
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "max": {
                        "speed": 25.04,
                        "direction": 181.56
                    },
                    "min": {
                        "speed": 5.21,
                        "direction": 145.35
                    },
                    "avg": {
                        "speed": 14.1,
                        "direction": 180.89
                    }
                }
            ],
            "humidity": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "max": 0.27,
                    "min": 0.08,
                    "avg": 0.13
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "max": 0.31,
                    "min": 0.1,
                    "avg": 0.19
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "max": 0.33,
                    "min": 0.07,
                    "avg": 0.17
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "max": 0.24,
                    "min": 0.07,
                    "avg": 0.14
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "max": 0.45,
                    "min": 0.17,
                    "avg": 0.3
                }
            ],
            "cloudrate": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "max": 0,
                    "min": 0,
                    "avg": 0
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "max": 0.95,
                    "min": 0,
                    "avg": 0.21
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "max": 0.96,
                    "min": 0,
                    "avg": 0.2
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "max": 0,
                    "min": 0,
                    "avg": 0
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "max": 1,
                    "min": 0.03,
                    "avg": 0.44
                }
            ],
            "pressure": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "max": 101032.3,
                    "min": 99945.69,
                    "avg": 100146.39
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "max": 100139.24,
                    "min": 99512.3,
                    "avg": 99898.08
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "max": 99899.24,
                    "min": 99283.29,
                    "avg": 99619.78
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "max": 99556.84,
                    "min": 98963.29,
                    "avg": 99330.02
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "max": 99659.24,
                    "min": 99019.24,
                    "avg": 99328.44
                }
            ],
            "visibility": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "max": 24.13,
                    "min": 8.86,
                    "avg": 9.8
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "max": 21.04,
                    "min": 11.22,
                    "avg": 14.12
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "max": 33.67,
                    "min": 16.84,
                    "avg": 21.64
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "max": 33.67,
                    "min": 21.04,
                    "avg": 25.74
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "max": 33.67,
                    "min": 15.3,
                    "avg": 25.05
                }
            ],
            "dswrf": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "max": 834.7,
                    "min": 0,
                    "avg": 511.7
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "max": 812.3,
                    "min": 0,
                    "avg": 325.3
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "max": 824,
                    "min": 0,
                    "avg": 331.8
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "max": 828.7,
                    "min": 0,
                    "avg": 333.5
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "max": 782.4,
                    "min": 0,
                    "avg": 310.5
                }
            ],
            "air_quality": {
                "aqi": [
                    {
                        "date": "2020-04-28T00:00+08:00",
                        "max": {
                            "chn": 99,
                            "usa": 99
                        },
                        "avg": {
                            "chn": 86.85,
                            "usa": 86.85
                        },
                        "min": {
                            "chn": 65,
                            "usa": 65
                        }
                    },
                    {
                        "date": "2020-04-29T00:00+08:00",
                        "max": {
                            "chn": 81,
                            "usa": 81
                        },
                        "avg": {
                            "chn": 74.83,
                            "usa": 74.83
                        },
                        "min": {
                            "chn": 64,
                            "usa": 64
                        }
                    },
                    {
                        "date": "2020-04-30T00:00+08:00",
                        "max": {
                            "chn": 69,
                            "usa": 69
                        },
                        "avg": {
                            "chn": 63.75,
                            "usa": 63.75
                        },
                        "min": {
                            "chn": 56,
                            "usa": 56
                        }
                    },
                    {
                        "date": "2020-05-01T00:00+08:00",
                        "max": {
                            "chn": 64,
                            "usa": 64
                        },
                        "avg": {
                            "chn": 59.83,
                            "usa": 59.83
                        },
                        "min": {
                            "chn": 52,
                            "usa": 52
                        }
                    },
                    {
                        "date": "2020-05-02T00:00+08:00",
                        "max": {
                            "chn": 71,
                            "usa": 71
                        },
                        "avg": {
                            "chn": 60.75,
                            "usa": 60.75
                        },
                        "min": {
                            "chn": 50,
                            "usa": 50
                        }
                    }
                ],
                "pm25": [
                    {
                        "date": "2020-04-28T00:00+08:00",
                        "max": 74,
                        "avg": 64.62,
                        "min": 44
                    },
                    {
                        "date": "2020-04-29T00:00+08:00",
                        "max": 60,
                        "avg": 54.96,
                        "min": 46
                    },
                    {
                        "date": "2020-04-30T00:00+08:00",
                        "max": 50,
                        "avg": 46.12,
                        "min": 40
                    },
                    {
                        "date": "2020-05-01T00:00+08:00",
                        "max": 46,
                        "avg": 43,
                        "min": 37
                    },
                    {
                        "date": "2020-05-02T00:00+08:00",
                        "max": 52,
                        "avg": 43.67,
                        "min": 35
                    }
                ]
            },
            "skycon": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "value": "CLEAR_DAY"
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "value": "PARTLY_CLOUDY_DAY"
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "value": "CLEAR_DAY"
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "value": "CLEAR_DAY"
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "value": "PARTLY_CLOUDY_DAY"
                }
            ],
            "skycon_08h_20h": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "value": "CLEAR_DAY"
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "value": "CLEAR_DAY"
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "value": "CLEAR_DAY"
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "value": "CLEAR_DAY"
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "value": "PARTLY_CLOUDY_DAY"
                }
            ],
            "skycon_20h_32h": [
                {
                    "date": "2020-04-28T00:00+08:00",
                    "value": "CLEAR_NIGHT"
                },
                {
                    "date": "2020-04-29T00:00+08:00",
                    "value": "PARTLY_CLOUDY_NIGHT"
                },
                {
                    "date": "2020-04-30T00:00+08:00",
                    "value": "CLEAR_NIGHT"
                },
                {
                    "date": "2020-05-01T00:00+08:00",
                    "value": "CLEAR_NIGHT"
                },
                {
                    "date": "2020-05-02T00:00+08:00",
                    "value": "LIGHT_RAIN"
                }
            ],
            "life_index": {
                "ultraviolet": [
                    {
                        "date": "2020-04-28T00:00+08:00",
                        "index": "4",
                        "desc": "强"
                    },
                    {
                        "date": "2020-04-29T00:00+08:00",
                        "index": "3",
                        "desc": "中等"
                    },
                    {
                        "date": "2020-04-30T00:00+08:00",
                        "index": "4",
                        "desc": "强"
                    },
                    {
                        "date": "2020-05-01T00:00+08:00",
                        "index": "4",
                        "desc": "强"
                    },
                    {
                        "date": "2020-05-02T00:00+08:00",
                        "index": "2",
                        "desc": "弱"
                    }
                ],
                "carWashing": [
                    {
                        "date": "2020-04-28T00:00+08:00",
                        "index": "2",
                        "desc": "较适宜"
                    },
                    {
                        "date": "2020-04-29T00:00+08:00",
                        "index": "2",
                        "desc": "较适宜"
                    },
                    {
                        "date": "2020-04-30T00:00+08:00",
                        "index": "1",
                        "desc": "适宜"
                    },
                    {
                        "date": "2020-05-01T00:00+08:00",
                        "index": "3",
                        "desc": "较不适宜"
                    },
                    {
                        "date": "2020-05-02T00:00+08:00",
                        "index": "3",
                        "desc": "较不适宜"
                    }
                ],
                "dressing": [
                    {
                        "date": "2020-04-28T00:00+08:00",
                        "index": "3",
                        "desc": "热"
                    },
                    {
                        "date": "2020-04-29T00:00+08:00",
                        "index": "3",
                        "desc": "热"
                    },
                    {
                        "date": "2020-04-30T00:00+08:00",
                        "index": "3",
                        "desc": "热"
                    },
                    {
                        "date": "2020-05-01T00:00+08:00",
                        "index": "2",
                        "desc": "很热"
                    },
                    {
                        "date": "2020-05-02T00:00+08:00",
                        "index": "2",
                        "desc": "很热"
                    }
                ],
                "comfort": [
                    {
                        "date": "2020-04-28T00:00+08:00",
                        "index": "4",
                        "desc": "温暖"
                    },
                    {
                        "date": "2020-04-29T00:00+08:00",
                        "index": "4",
                        "desc": "温暖"
                    },
                    {
                        "date": "2020-04-30T00:00+08:00",
                        "index": "4",
                        "desc": "温暖"
                    },
                    {
                        "date": "2020-05-01T00:00+08:00",
                        "index": "4",
                        "desc": "温暖"
                    },
                    {
                        "date": "2020-05-02T00:00+08:00",
                        "index": "3",
                        "desc": "热"
                    }
                ],
                "coldRisk": [
                    {
                        "date": "2020-04-28T00:00+08:00",
                        "index": "4",
                        "desc": "极易发"
                    },
                    {
                        "date": "2020-04-29T00:00+08:00",
                        "index": "4",
                        "desc": "极易发"
                    },
                    {
                        "date": "2020-04-30T00:00+08:00",
                        "index": "4",
                        "desc": "极易发"
                    },
                    {
                        "date": "2020-05-01T00:00+08:00",
                        "index": "4",
                        "desc": "极易发"
                    },
                    {
                        "date": "2020-05-02T00:00+08:00",
                        "index": "4",
                        "desc": "极易发"
                    }
                ]
            }
        },
        "primary": 0
    }
}
```



## 搭建 MVVM 项目架构

MVVM（Model–View–ViewModel）是一种高级项目架构模式，目前已经广泛应用在 Android 程序设计领域，类似的架构模式还有 MVP、MVC 等。

简单说来讲，MVVM 架构可以将程序结构主要分为 3 部分：

- Model

  数据模型部分

- View

  界面展示部分

- ViewModel

  可以理解成一个连杰数据模型和界面展示的桥梁，从而实现让业务逻辑和界面展示分离的程序结构设计

MVVM 项目架构示意图。

![](../images/chapter15/mvvm.png)

UI 控制层包含平时所写的 Activity、Fragment、布局文件等于界面相关的东西。

ViewModel 层持有和 UI 元素相关的数据，以保证这些数据在屏幕旋转时不会丢失，并且还要提供接口给 UI 控制层调用以及和仓库层进行通信。

仓库层主要工作是判断调用方请求的数据应该是从本地数据源中获取还是从网络数据源中获取，并将获取到的数据返回给调用方。本地数据源可以使用数据库、SharedPreferences 等持久化技术来实现，而网络数据源则使用 Retrofit 访问服务器提供的接口来实现。

所有箭头都是单向的，谨记每一层组件都只能与它相邻的组件进行交互。

---

**包结构**

```
com
  └─homurax
      └─sunnyweather
          │  MainActivity.kt
          │
          ├─logic
          │  ├─dao
          │  ├─model
          │  └─network
          └─ui
              ├─place
              └─weather
```

- logic：业务逻辑相关的代码
  - dao：数据访问对象
  - model：对象模型
  - network：网络相关的代码

- ui：界面展示相关的代码
  - place、weather：两个主要界面

---

**依赖库**

```
/* RecyclerView */
implementation 'androidx.recyclerview:recyclerview:1.1.0'
/* Lifecycle */
implementation "androidx.lifecycle:lifecycle-extensions:2.2.0"
implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:2.2.0"
implementation "androidx.lifecycle:lifecycle-livedata-ktx:2.2.0"
/* WorkManager */
implementation "androidx.work:work-runtime:2.3.4"
/* Material */
implementation 'com.google.android.material:material:1.1.0'
/* Retrofit */
implementation 'com.squareup.retrofit2:retrofit:2.8.1'
implementation 'com.squareup.retrofit2:converter-gson:2.8.1'
/* 协程 */
implementation "org.jetbrains.kotlinx:kotlinx-coroutines-core:1.3.5"
implementation "org.jetbrains.kotlinx:kotlinx-coroutines-android:1.3.5"
```

## 搜索全球城市数据

搜索具体城市数据 → 获取该地区的经纬度坐标。

### 实现逻辑层代码

ViewModel 不持有 Activity 的引用了，需要提供全局获取 Context 的方式。

***SunnyWeatherApplication***

```kotlin
class SunnyWeatherApplication : Application() {

    companion object {
        // 彩云天气 API token
        const val TOKEN = "..."
        @SuppressLint("StaticFieldLeak")
        lateinit var context: Context
    }

    override fun onCreate() {
        super.onCreate()
        context = applicationContext
    }
}
```

***PlaceResponse.kt***

```kotlin
class Location(val lng: String, val lat: String)

class Place(val name: String, val location: Location,
            @SerializedName("formatted_address") val address: String)

class PlaceResponse(val status: String, val places: List<Place>)
```

JSON 中一些字段和 Kotlin 字段命名不一致，通过 `@SerializedName` 注解的方式来建立映射关系。

***PlaceService***

```kotlin
interface PlaceService {

    @GET("v2/place?token=${SunnyWeatherApplication.TOKEN}&lang=zh_CN")
    fun searchPlaces(@Query("query") query: String): Call<PlaceResponse>

}
```

***ServiceCreator***

```kotlin
object ServiceCreator {

    private const val BASE_URL = "https://api.caiyunapp.com/"

    private val retrofit = Retrofit.Builder()
        .baseUrl(BASE_URL)
        .addConverterFactory(GsonConverterFactory.create())
        .build()

    fun <T> create(serviceClass: Class<T>): T = retrofit.create(serviceClass)

    inline fun <reified T> create(): T = create(T::class.java)

}
```

***SunnyWeatherNetwork***

```kotlin
object SunnyWeatherNetwork {

    private val placeService = ServiceCreator.create(PlaceService::class.java)

    suspend fun searchPlaces(query: String) = placeService.searchPlaces(query).await()

    private suspend fun <T> Call<T>.await(): T {
        return suspendCoroutine { continuation ->
            enqueue(object : Callback<T> {
                override fun onResponse(call: Call<T>, response: Response<T>) {
                    val body = response.body()
                    if (body != null) {
                        continuation.resume(body)
                    } else {
                        continuation.resumeWithException(RuntimeException("response body is null"))
                    }
                }

                override fun onFailure(call: Call<T>, t: Throwable) {
                    continuation.resumeWithException(t)
                }
            })
        }
    }

}
```

当外部调用 SunnyWeatherNetwork 的 `searchPlaces()` 函数时，Retrofit 就会立即发起网络请求，同时当前协程也会被阻塞住。直到服务器响应我们的请求之后，`await()` 函数就会将解析出来的数据模型对象取出来并返回，同时恢复当前协程的执行，`searchPlaces()` 函数在得到 `await()` 函数的返回值后将该数据返回到上一层。

***Repository***

```kotlin
object Repository {

    fun searchPlaces(query: String) = liveData(Dispatchers.IO) {
        val result = try {
            val placeResponse = SunnyWeatherNetwork.searchPlaces(query)
            if (placeResponse.status == "ok") {
                val places = placeResponse.places
                Result.success(places)
            } else {
                Result.failure<List<Place>>(RuntimeException("response status is ${placeResponse.status}"))
            }
        } catch (e: Exception) {
            Result.failure<List<Place>>(e)
        }
        emit(result)
    }

}
```

Repository 中定义的方法，为了能够将异步获取的数据以响应式编程的方式通知给上一层，通常会返回一个 LiveData 对象。

`liveData()` 函数是 `lifecycle-livedata-ktx` 库提供的功能，它可以自动构建并返回一个 LiveData 对象，然后在它的代码块中提供一个 suspend 函数的上下文。

`emit()` 方法类似于调用 LiveData 的 `setValue()` 方法来通知数据变化。

***PlaceViewModel***

```kotlin
class PlaceViewModel : ViewModel() {

    private val searchLiveData = MutableLiveData<String>()

    val placeList = ArrayList<Place>()

    val placeLiveData = Transformations.switchMap(searchLiveData) { query ->
        Repository.searchPlaces(query)
    }

    fun searchPlaces(query: String) {
        searchLiveData.value = query
    }

}
```












