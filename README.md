# rekognition_video_analysis

## 動画からのシーン検出および物体検出

詳細は下記に記載

https://docs.aws.amazon.com/cli/latest/reference/rekognition/get-label-detection.html

### ラベル検出の実行

AWS CLI:

```sh
aws rekognition start-label-detection --video "S3Object={Bucket={Bucket_name}, Name={Path_to_Video_File}}"
```

返り値にJobIDが表示されるのでコピーしておく

```JSON
"JobId": "e6fab58dcdb79c3641d8f918e73a46c05d0efa417f7182770f4ce812b6c8fd6a"
}
```

### 実行結果の取得

AWS CLI:

```sh
aws rekognition get-label-detection --job-id {JobId}
```

