NRCPrefix
=========

Prefixer for Myanmar National Registration Card's Format

## Match Formats

`[State Number]\[District]([NAING/N])[Register No]`

- `12/MYK(N)167887`
- `12/MAYAKA(N)167887`
- `12/MYK(NAING)167887`

Prefer formats
- `12/MAYAKA(N)167887`
- `12/MAYAKA(NAING)167887`
- `၁၂/မရက(နိုင်)၁၆၇၈၈၇`

*NOTE*

Three english characters in district are not complete format and will not support some function.
So you should be use six english characters for district.

## Usage
### Get format

```js
var nrc = MMNRC("12/Mayaka (NAING) 167887");

nrc.getFormat() // 12/MAYAKA(N)167887
nrc.getFormat("mm") // ၁၂/မရက(နိုင်)၁၆၇၈၈၇
```

### Test Equal

```js
var nrc = MMNRC("12/OUKAMA (N) 123456");

nrc.isEqual('၁၂/ဥကမ(နိုင်)၁၂၃၄၅၆') // return true;
```

### Get State name from nrc card

```js
var nrc = MMNRC("12/MAYAKA(N)167887");

nrc.getState("mm") //ရန်ကုန်တိုင်း
nrc.getState() // YANGON
```
