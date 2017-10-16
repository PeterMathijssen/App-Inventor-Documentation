# **DatePicker**

A button that, when clicked on, launches a popup dialog to allow the user to select a date.

#### **Events**

* AfterDateSet\(\): Event that runs after the user chooses a Date in the dialog.

![](https://lh6.googleusercontent.com/XwOWtPgSmgQQLT-1jqEV_6DGsxOFb5UwFSfSHCgUesYHBUksCyGolV5ndcfkfEe_WszTPUIGIZ-Xa-YL0WZdZ_Qz-tuvD7s0z5BX1zN2VjFS-dJ70s50s9kCY5cAxroSHrf13ylv)

* GotFocus\(\): Indicates the cursor moved over the button so it is now possible to click it.

![](https://lh6.googleusercontent.com/vH-lr8e1MHdVgwtg_LAbQMebEbH7AsxjgQXU8vhEFS3MdOrH2AuLdNJ6GxuAuBj8yoj8HVfXl1QIaGgunzSjxXeTwvhePvZ7GODv9rIT2z_GkYASrYCTl7KzGHH8a_2qdMBVSjXd)

* LostFocus\(\): Indicates the cursor moved away from the button so it is now no longer possible to click it.

![](https://lh3.googleusercontent.com/38ZN5WM41zXw4SSt9-GOOP-N67FPI9Jcqi7C1K6J9xiFlG-NbdfzSEoNLLJET0s087KPh4lMV5IsAvxMqZTYTRoPBvUeLrwD84Pk3SHOdtTB6K57xHm36Xtvfp3E24mlAmWViCFH)

* TouchDown\(\): Indicates that the button was pressed down.

![](https://lh4.googleusercontent.com/-ikLyLfFRAiIYmij0XK69Qjuw6VSFC5YJHKWAQR6_IDP6bUeeixQSTX6vW_bRinWhc9uNJ1vLaAfqMVbuQq19BWfRBGA1awx64OFfGqMH19SHRMHc5GHp0Un6fmiKpczGGz4im0J)

* TouchUp\(\): Indicates that a button has been released.

![](https://lh4.googleusercontent.com/0xWZNbdUPn0yGJaZHlUSrN6XemrRtiF7bNYSEpum1KYPQlKQ1Vo9djZeQ1oUds-nThjV4_ipPe-S3MCx3mL2xgIiwGD_Yp_bmKxWhqBvPC1f7CMgU3RFwEh_dOqvP6aBWeVGEFXK)

#### **Methods**

* LaunchPicker\(\): Launches the DatePicker popup.

![](https://lh5.googleusercontent.com/mD269N1gcjeAQLldwRhaiQs3nEQr7Sm7VRondflzrydsNoGMfsK4lKkc8mT4l_5xKboGKaZO_61BE0HZEeKs8mnV4fW7L7ktXDLwxWaS_rx8_D_ov045NiXrgdoFhtNqH-wIunG_)

* SetDateToDisplay\(number year, number month, number day\): Allows the user to set the date to be displayed when the date picker opens. Valid values for the month field are 1-12 and 1-31 for the day field.

![](https://lh3.googleusercontent.com/kZkw47ffpZvNu02FmIywHDqa3ROb4Rr_fPB_X4IbXtF54Wa1XrNU209fb9SGArdIBrdTFI-qpiIoig3j3gDCn3QbcCH_UtcaHQ_4RV0JPsCXd3R2XK5hEtCH1qyjfTdyhl88PoXw)

* SetDateToDisplayFromInstant\(InstantInTime instant\): Allows the instant to set the year, month, and day to be displayed when the date picker opens. Instants are used in Clock, DatePicker, and TimePicker components.

![](https://lh6.googleusercontent.com/PYrbIdgoN4svPWI-qbP8z6fPQHZqk5vt2mslc5B1hZrFl0H_8vV0oj0TEwP8ETYGh1PTZaUecGeBwUDTKuxtj6vSvsAS2pkSNLBRAPHx5vrRFG4gWXd7Qali8HUZhdeAT091F0o8)

* SetShadow:

![](https://lh5.googleusercontent.com/udFJZ960dpu111nZfPImJgjTki5Oa-Q80BktI69OwTRJ8Yq9IwUvYe97-lgrVqbhAfJukvkxnR-eSGumEEPPHWJbAyOHFJFGaek0Amgsb55iQo2_5JVVv54yf-lFAi3fEPY0yXK7)

#### **Properties**

* BackgroundColor: Returns the button's background color. Also available in the Designer properties.

![](https://lh5.googleusercontent.com/mjsXsPv2LlBPTEKT61hpZqrd44pjLoCd4_KyNpKCe2DRRPGaZX_I_9QO3oChdMI1ZpBWwCSXn3tQgUV4M67cO8MLdJKMjSttegaRGDEE2SnGVenUIF4fJVMR3kj6iQ_X9gkr600n)![](https://lh6.googleusercontent.com/vO5zx_cb46g57-MKoxN_BbDHqlbB93HYczT5NkLvdycwba-VhG8OinAS9S2e6nD23k2j7ky478Q3mg1mL9n0SIPuM1S-30putyaGNhFAb5WPd5pbx3Rf5yqCm_SkMCZ4NiG-UMad)

![](https://lh5.googleusercontent.com/LE2bQycGbC0TfazYbGq8f4Tw0JdEZuXTVZhav42QSk9ZVkNK_qMuRLlrYEq0_6VZIhtb5R6ECVeURU-G3FinufhYsMZCyEfsL4i68VCL32eggQvpP9UR8U6h_NZPFgEWkdjNWWR-)

* Day: the Day of the month that was last picked using the DatePicker.

![](https://lh5.googleusercontent.com/4QLFVlhuCC6ngEdRJLDtg54yNdGy66NZBJMLf8QjOQ2nGBRV5M4rOmQXTt5Ujqs6tyCzkU_aItpSdeaSelnJKAZJeDA7Yeol14SAaT7xey1oHlGfBNbYbHk6MAHM4d7-7mR95-SP)

* Enabled: If set, user can tap check box to cause action. Also available in the Designer properties.

![](https://lh3.googleusercontent.com/bQnYlRluyswO7A9iSPOMNo2K-nUPnmLaJCA7v2w65_tXn3eyL85YP6vKLulOGnh3yCs4gnCVCczlqlplHGlUAdIFh9_BTw-6a35RB20AZgiIloWpQTVPIHLyWJsFibfX4vGOH0zg)![](https://lh5.googleusercontent.com/_3kguKt2nq-TWGm1SO9xec9DWz6AvQXLfaxHCdDlc2y7QQfwbWnwXVhxXmi5I8aT34A5u47yx02mDuQgMcNbrMqXltvyZHL1bb_t1orm3zXEEzuaOtKVrWJeD7YVidQQUunz6f6x)

![](https://lh5.googleusercontent.com/pOnTUcOJF5ealZZiGQe_Nfoldu44_Dwmb5hD4R73dJUosoiJnz8FG17tO67SYfCS76pEG8-ZLnHbLuLUDwDiJGBphxLpnEnQShVKHovu7ah4BcuHSY-sjflUMAykaVJoUcuIxuPs)

* FontBold: If set, button text is displayed in bold. Also available in the Designer properties.

![](https://lh4.googleusercontent.com/LAk-T490A6Q5Vu0tf9Z4SvnFLvPXIaWjB_smxzX47qwX75Qzan9gC1G52yvpD-Q-HD4_2s9l0T2kq-UTH-jDxoZDu-LQfI2BtEheUIX8Uf18MXb2RaBLERLfTxA_RiiI6ghWUTQD)![](https://lh3.googleusercontent.com/OZYrq2qefm1ihtYoqcO8O9PytC4EfH2Ogm85iC1Q4Bj2IEHlJsqZTCJhPDMvgg1UHgE8iKPAydSfAu6SVxjFGxceOO_tk3xHEYyi1c7L5__TbUjJCQbJcx9y9WgqYLV1gp6dlGz5)

![](https://lh6.googleusercontent.com/QhSpJDK71l2XWqQpOWA3UpxSsTSL9_kzySwNrcCkx2bM47VFdEJ-KULP2NUXS1eVFU_0G5TybV6WPjbuzzHVSpgBhPSAH7KzMl4BJv3Wgepsv_hiaDGt2hK4jGpNslVxrxuMf7_k)

* FontItalic: If set, button text is displayed in italics. Also available in the Designer properties.

![](https://lh5.googleusercontent.com/XwFHDZxGvnUwjW6iHyLj6Cw-qVYQWa5xeGD7XLn6Qp1HGddOyM2qodh47eKUpub8zxPZW-ph50CiDLnaKPWjkHrYKRMGw1zYFieyfvBmRCDtcNDXixbNftKdpCX5RRiQOYGvfTAG)![](https://lh3.googleusercontent.com/Dg0mMrDXrCPdwhlj3duyPNHj4-jvuCFiSi4c8NsOe2_Q1-gXaeakfNtTkBRR3gDRV_jpYkw5cb_q6arsL83K6BRydN3CAF7-pVCI8fX4_BZmtNo2BCIY7HGXMfDsJJuADqBY94vO)

![](https://lh5.googleusercontent.com/NMzlo8Qc2nRx6sZvnAeUA8sQOLePmQ_mvft3awge0MCzeCghz0Jt5BZ9yhecv9hN4o5o-G3zidsZHy7qhCJ16Wf8U48gl2c7laVTueyEQEokjPB9eWos5pZsoJkEgi8FUNHqfUdP)

* FontSize: Point size for button text. Also available in the Designer properties.

![](https://lh5.googleusercontent.com/_h_tOdG93MgyodcTCN0GN04_JJVjveFcTHzCqNa59gN8H1oya4QxV6lBzxlwPbFcLGLR8DY3gzQ9HFYnRAz9RLy35LBY6ZnbJdxlrE16SvkqS2_ZYXZ5Vu-MfyZYm7Ck01RsV0Yu)![](https://lh5.googleusercontent.com/zi8i9BRcJ5P2p2aPWlHm1zIDN--2BCTeqY2AaG_sag2Po22Ru4aGgU-KWIFmIsi2MVm_T0n9a-BRCWjAqC3qNgYfzmfSmEYkANMIXZLE7AHYPZd5I3Ox6KKl1zaVuFoJuJMftBJO)

![](https://lh6.googleusercontent.com/SncGfoG-iKerxML8AtnuVq_Spg2p2pofTQZBe2e2T33nxNO_h7CKZ113aUzb7sTbqDgwhkBF8V4WU9P77XwFaZD3imjhphnx08CnA6QS1g1oZ9CyejXIgbbv73jnhaPvPf5ZNYUY)

* FontTypeface \(designer only\): Font family for button text.

![](https://lh4.googleusercontent.com/LjwObVroppE_34xAlDYmeGFzrLOTo_ynS8E_1fnavEDs4cI5QU7fSKs8MX_0kwVg1xTOQO3UHXxQDrIngpISgon1Ki0XXbzKxmNKtNJNwxCbBFy24Qf32_c6CWEahb5ipAGH6wqw)

* FontTypefaceCustom. Also available in the Designer properties.

![](https://lh6.googleusercontent.com/JemwwfBAvZbnVjwAsRkllkdVo-tXSwDMSz1HZpJLtlVff2mTE0Ns15P71tEIUnYkZXm0t8gNjoYfZHWyMJPxKIjZ1cMdBEW-7egjqtYzWt0r5psSGnc8ppUe20mVdtoAbsjdfzRT)![](https://lh4.googleusercontent.com/jYhzQCCE1AsgtK1JwEs8L7oWi5TTiB3nVlcbB3bo_NAM4KP_raaVb1Jy58s-IgAMhTAVC7q_0rvDyH62OlHW4XSyy6AfdRnDBIn9R8hsNJAcPC_w8m7U86IAYI8kG6fYF4Dc53pZ)

![](https://lh5.googleusercontent.com/NjeZ9WxWubOUzSxpwC1Mz3s9342Rlo5M3OquU8dGLPWLwH3s5o8Z572IzwVxayp74DRusfXFw4IzQVREreyowhOtTK3FHAU5oNOcZ8kYDD4Ta27FF9fqGqgDVog_9yV46N-Ji9-w)

* Height. Also available in the Designer properties.

![](https://lh3.googleusercontent.com/WJyh6JIxgV_7WZzH1sXS0bZSc0rjnpqfX7o_Fb5sHVKgAhxWuGwGQjqLW3n_4_FtQD1desh6l4Fb0k9HMlNesdKpNsPTZSnh4ehgM3aeXAUVBLPsQqV9sMI9Fj_8TwoWg3JnH40y)![](https://lh5.googleusercontent.com/phDOoAfDpph1Ce8NUbDDOiIEclQwBAJrr2paBtpcntokroUxhieaUMKelrelbCLoGHyKhDVaQTXMaEn-IDUnI6yelwDU0NZA4wlqnYMTaB96giKXcti4g5HLdDeKI95_i0xfOFwc)

![](https://lh5.googleusercontent.com/FgdgcP0aPr2z2S73tEIxgKyWm1gqUAckpDnC3j2ROjvqZ5JGGesDGYZ0KZ4KQTdWbpsYJMTrhhMhJys0m2PgitKCOjM1Nduh0RapqZ8KBD67f7AxhpWAhayirUKMBzH4xUCi5FqE)

![](https://lh5.googleusercontent.com/sfVh2-bBhO5aoeDUtyX2SFCd7NihyBH1EmnRDc3q-Kx5RJw2jnvlXTlyHgbC9wGrb18iPko18uR1IyvOpC-FiMaMcYVHKrRX8ockhbUX0L7gIydVzgBNsZVsTFtTw9_8ri0WvSxz)

* Image: Image to display on button. Also available in the Designer properties.

![](https://lh3.googleusercontent.com/LUnzUcu0AbvYqPQh4A28yfcwyXzH81jFe2uTv4nNcJyBB1j4j8lU1SRfsXA-TvkdCqes0Q98XQk0DaztQjJ6oP10N5fPEGrfuD7YFILvivj5zkKQzD3V0K6NIE3LGKP_L8aOpU2U)![](https://lh5.googleusercontent.com/yTwXSZG2gybkRN7ETeewEijtUd7giW47u6zY6bwtSKDSlvC2eZTppA45PnK3MmH6E-UhcnZ9ldjZi269zzMWOfqxXX1ll8oyEGrUcy-G_byEiIvRIRru90whRZLRCNe5wOG0DHkE)

![](https://lh4.googleusercontent.com/rM6915J782yBB8nsXoIS4gelCutYeBGJbkLFwSawIe_qkGUs-DHKvtthXo6IW9zP4IonqIhHRBtNfrNQPzu8UbexRfAevwBwrQzJbklfx2hK8DVKPWLkD8o1naTryItNS5nQA5ch)

* Instant: Instant of date. This instant can be used with Clock component for date documentation, conversion, and matriculation.

![](https://lh4.googleusercontent.com/O3jWhOjK3VmvYiO0aoabtcRHyjBhYn7t9z1tjlaQUc4eRno7Ve2sNTz3noywfZ0HGxkhcVFpIyu0nLWZryDXAVczPPezPQaaO5VRJ8IYjtkcm46qFG-l-nvh90AYfKWVyPV3Sr4R)

* Month: the number of the Month that was last picked using the DatePicker. Note that months start in 1 = January, 12 = December.

![](https://lh4.googleusercontent.com/7qBByEEtXdLGBsiD0vaxnFA4aGpzUjQACKZWRoQOLXs22UM1SqhD0fTRw1l-vxr778i0vqtt350tYJu1DofNhkdjJc9dogud1601T3js73sGFARhAo8n0QCZxNmCqGnLDkYfHwqQ)

* MonthInText: Returns the name of the Month that was last picked using the DatePicker, in textual format.

![](https://lh4.googleusercontent.com/B1O-v7OYmTlGS08dJ73Xm9x_R6FjBokmWTUGD68vCwpTEso-ML12B3MRIE17wZMSFjeVU-DG8xiBrll0JqfJlcUZXeyVH7Q0s-in0Hxyak_Rdixqp2tn6mq_KJPWLIzJGddf7r3m)

* Shape \(designer only\): Specifies the button's shape \(default, rounded, rectangular, oval\). The shape will not be visible if an Image is being displayed.

![](https://lh4.googleusercontent.com/-VSaSdaLp6jgqtrrixPyhyDTYyyVZOUPsTnFYwIyjUFgFax4Sxztlc3xEwni05d-Q4SreuBSfpXdUQ6B30Yq3BXu1ZLaYl0wnJh0iXsg3F6qReINeX54aM7TmxSRy0j5YB721e-F)

* ShowFeedback: Specifies if a visual feedback should be shown for a button that as an image as background. Also available in the Designer properties.

![](https://lh4.googleusercontent.com/oRd1wRLYR7QEP2RAQ6SMujC5aD1CT_LDf4J3kG1M1B7L8gNsIihvMyheDW8o7uGcpD1qRn1mpWWDb9EeOiekt_NS61g9YGayqtV3x6038XbJznLVRqRnf3B3oef0zqv8_fYPcevF)![](https://lh6.googleusercontent.com/NromG9LTr9PBiRE9H3RVq8CxyT1F7-F8deUlQ7alGZ8g2wDh-eTlHzb9Hz9AAJ4xzshJEprKictyg12iukGzGpRc3IjyAMjt9z0jdTNN3lIVen2jgEgIgaOZ-tVLQXLLur9kNPj_)

![](https://lh4.googleusercontent.com/44LV_QddOagjvtEw-6MUQq-krka1-jPxl1czgKkkiVcA-DDjhIGzjh4nZleh5vMqin_WAAYBwS1c4P7TjxQpL368MufBr0wsWBTCjIdBQekEWGLJ2IOqzvsAh0eQMjDe0Ov5Xlbb)

* Text: Text to display on button. Also available in the Designer properties.

![](https://lh4.googleusercontent.com/VHhMxhWobc_Ur1sIQiHZhrx8069LsCRdVK-WhbaEGnKJgIpYJ-kr8WWAoT7qux9ghZljtRxaosPghlZdPruajxYPPBYs3Ekj_AwEulvs7ZlW2OB8EDXLBwXjz7ZXeoiu67yyq6pd)![](https://lh3.googleusercontent.com/xaJx6N7hIjt-xQ0YLX-YP_lbBVTZluwEZA_9HB-6Z5leO-GNvdMfEYFZqda5rrVuuMp-ZEuc09etajrZlhN3bQ9NCQXJWS_Doou_jD3up6f8VjHnVHs4j536D8inDoxPYNzZIP6a)

![](https://lh6.googleusercontent.com/HmjuaFtiNt9ogsswWRdqSxRY0F6C6cW8-7gjbqXlsOfBd0CFUcvnSkAZxVSMraohjXPZxFYN2VHBMvIiB2rQZ-37AQ01z7nmjtWfFawaG6sCh92IjVoMWQyospIGDuU6UKOtMDzU)

* TextAlignment \(designer only\): Left, center, or right.

![](https://lh6.googleusercontent.com/RvDrw7eAVBlFKj8L-X8azfefHlgDcphmG-Uwjw7PJ12Jz4okfLT0b-AMVa68mHZat6RYJQVAh2b-dg28Znyt1aBia1CR_u2c1s1zY11Mqb1Gl1imwPgubAsm0F0-2Q7Ar1xpnA1m)

* TextColor: Color for button text. Also available in the Designer properties.

![](https://lh5.googleusercontent.com/oKrBpVjMOilLmw--Y8Wd2P7rOjVYY-Kbm3ZGyIUbb7uGvQMWGKQ43YMpGkdIQXOktTZpEN1wcsB28oZXNoMMSkJv9iUZGZJqUdINRP1DR6IhUpUkNjzHcmQQgjMVhF9HaXclOc0X)![](https://lh5.googleusercontent.com/Mck1yANgnEw6dmdig7h3p-LdYLMqXrCqvfs-8k3vmlldRkZvvPrCfuNAKq6sJ8TCJ9G3HhNDKltbHfLYlPavJweYcgSpePzlET-iuLSSna4u2PADnu3D4YgOW2BxHa7dWXoPfPK4)

![](https://lh6.googleusercontent.com/7XnYcgBUlMoL7fPAZ9_MI6sBEqAnZl_4e3QAcW_sq0gr2rtDBcBk0Wgty4qGz5IR_BZsiei4LTFQr_N6glzkTE7I7hGOO2hXic89vzmFQcQHRFbWhA8_PAnzFrHOY6keWW7Gkagg)

* Visible: Specifies whether the component should be visible on the screen. Value is true if the component is showing and false if hidden. Also available in the Designer properties.

![](https://lh3.googleusercontent.com/irR8cUDSkNakvWp0Ch23JR6mCdoZudsx00wKrLjOyJECWhkQdWV0JhDvV8U5fkEDV4LbE3upsoOf6eAeaDiVgISborcw6alsVSGtIwbFylYG8iTYco0sV6F17Ufch6vTLgn4K-_6)![](https://lh3.googleusercontent.com/HWfQCZUZvGnanmApqF9N5tvwjSDI6HliGZA-J6_4DqTwXXVqy_HMQAfMWz3F8w772OdQSlR510yXpqz9OfvApVrEZEQe12QVg8g-aLxjbjSnMCpsEES1g2qcEhAw2I5g88C1PTIy)

![](https://lh4.googleusercontent.com/YZ1mgF6faGjH07EIsoMy-pfaabTTUCmFTj1PcdAaKT-qtdgiVhlI3PkkbRp9uIQsMMDCGezatNO6XOZqZTwfwrmRtPb1iOyF5tcljmtfPSQ1MgvOdiDndSWUIkRsvsF0GQPS2TNA)

* Width: Also available in the Designer properties.

![](https://lh4.googleusercontent.com/6pUn9BE8jPPAhCZ3MoF3d19WLMSvoyEHvUwm0dXoZkseLcn2D-20rtQ6te5ddg6nGibUeRP8DOcLd8e-LJ3MlPqwtF-Lt7XVXFn01EseMuKMw90Yymd3JcPUPoat1VjhOVYrZkEL)![](https://lh4.googleusercontent.com/2Lin_WcvtBgwu4wJuZgKUKLNJ7FZZ6ACXS1fbWiAJVHeLHzwdQsXZU-hpwF-TgDV4-D_c-g6Modi0XOqLhtBexWs68kQDNGSlqNNQ6RAzwp77ljmBXyt5Eo9XI0CzqBa59OlxbFd)

![](https://lh4.googleusercontent.com/BHjzPpdl6w2k0XB7IrBpbtigS0Pin7LdcqCTCmcSy2gAL3jCvMFNH13Jf-abcCRm_Xq5trMx1fYWs6QA9Ou8Kjqtu48Xy_ardBOLyjjhkQy34yJsrx1vXZYZeT36ro97V4fdCxCp)

![](https://lh3.googleusercontent.com/k9-s309gUfRnXaP3sYZV2RkAgavLvP6LKW3_G-OJINAVjY2vw0ZaQcV21iuG1a1S7LRA1baUe3M7W1YRWf0zT5oTNOppmcGtvv79K8UDEK1ry3b8jpujN_6ulg4K_pr9sVIeji2C)

* Year: the Year that was last picked using the DatePicker.

![](https://lh5.googleusercontent.com/9otJXvshBjU7VUwDgBbjswi08aFZu81sxF3DjDFgnw8_MaFK8XxjYWOB3PdSJ7iwpzWBZTcR6KeCFpo1pvJODInjY5ca_lIDVvJVyNYnk7opljFFoN33rl7usN5dcg7rkSsaxc4M)

