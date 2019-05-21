# TransferRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | 口座ID 半角英数字 口座を識別するID  | [default to null]
**RemitterName** | **string** | 振込依頼人名 半角文字 指定しない場合は口座名義がデフォルト値となります 振込許容文字を指定可 ただし、一部の非許容文字は、許容文字に変換を行います  | [optional] [default to null]
**TransferDesignatedDate** | **string** | 振込指定日 半角文字 YYYY-MM-DD形式 振込対象の指定日 ただし、振込指定日が非営業日で、非営業日に実施できない振込（他行宛振込み）が振込情報に1件以上存在する場合、以下のとおりとなります ・「振込指定日休日コード」が1または省略の場合、振込指定日の翌営業日を振込対象の指定日となります ・「振込指定日休日コード」が2の場合、振込指定日の前営業日を振込対象の指定日となります ・「振込指定日休日コード」が3の場合、エラーとなり「400 Bad Request」を返却します  | [default to null]
**TransferDateHolidayCode** | **string** | 振込指定日休日コード 半角数字 1：翌営業日、2：前営業日、3：エラー返却 省略可（省略した場合は1とみなします）  | [optional] [default to null]
**TotalCount** | **string** | 合計件数 半角数字 1以上99件まで指定可能（0はエラー） 1件のみの場合は省略可（項目自体の設定が不要です）  | [optional] [default to null]
**TotalAmount** | **string** | 合計金額 半角数字 1以上999,999,999,999円以下　数値のみで0、カンマ、マイナス不可 1件のみの場合は省略可（項目自体の設定が不要です）  | [optional] [default to null]
**ApplyComment** | **string** | 振込申請メモ（申請コメント） 全半角文字 項目自体の設定が不要 値を設定しても銀行で読み捨て  | [optional] [default to null]
**Transfers** | [**[]Transfer**](Transfer.md) | 振込情報 振込情報のリスト  | [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

