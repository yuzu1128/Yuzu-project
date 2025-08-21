# 📥 データインポート手順

## 方法1: 移行ツールを使用（推奨）

1. **移行ツールを開く**
   https://yuzu1128.github.io/Yuzu-project/data-migration.html

2. **「データを自動インポート」をクリック**

3. **メインアプリで確認**
   https://yuzu1128.github.io/Yuzu-project/

---

## 方法2: 手動インポート（移行ツールでエラーの場合）

1. **メインアプリを開く**
   https://yuzu1128.github.io/Yuzu-project/

2. **ブラウザの開発者ツールを開く**
   - Windows: `F12` または `Ctrl+Shift+I`
   - Mac: `Cmd+Option+I`

3. **コンソールタブを選択**

4. **以下のコードをコピーして貼り付け、Enter**

```javascript
// データインポートコード
const importData = {
  subjects: [
    {id:1,name:"地理白地図（1265語）",target_questions:1265,deadline:"2026-08-16",unit:"ページ",order_index:1,created_at:"2025-08-16T14:14:06"},
    {id:2,name:"白チャA",target_questions:113,deadline:"2025-09-09",unit:"問",order_index:2,created_at:"2025-08-16T14:14:06"},
    {id:3,name:"白チャⅡ",target_questions:209,deadline:"2025-08-23",unit:"問",order_index:3,created_at:"2025-08-16T14:14:06"},
    {id:4,name:"白チャB",target_questions:60,deadline:"2025-09-09",unit:"問",order_index:4,created_at:"2025-08-16T14:14:06"},
    {id:5,name:"地理白地図復習",target_questions:999,deadline:"2026-03-11",unit:"ページ",order_index:5,created_at:"2025-08-16T14:14:06"},
    {id:6,name:"白チャ復習",target_questions:999,deadline:"2026-03-11",unit:"問",order_index:6,created_at:"2025-08-16T14:14:06"},
    {id:7,name:"ネクステ文法復習",target_questions:9999,deadline:"2026-03-11",unit:"問",order_index:7,created_at:"2025-08-16T14:14:06"},
    {id:8,name:"ネクステ語法",target_questions:228,deadline:"2025-09-11",unit:"問",order_index:8,created_at:"2025-08-16T14:14:06"},
    {id:9,name:"ネクステ",target_questions:514,deadline:"2025-08-09",unit:"問",order_index:9,created_at:"2025-08-16T14:14:06"},
    {id:10,name:"ターゲット1900",target_questions:1900,deadline:"2025-08-09",unit:"個",order_index:10,created_at:"2025-08-16T14:14:06"},
    {id:11,name:"地理B一問一答⭐⭐⭐",target_questions:1789,deadline:"2025-08-09",unit:"問",order_index:11,created_at:"2025-08-16T14:14:06"},
    {id:12,name:"白チャI",target_questions:155,deadline:"2025-08-09",unit:"問",order_index:12,created_at:"2025-08-16T14:14:06"},
    {id:13,name:"白チャC",target_questions:66,deadline:"2025-09-09",unit:"問",order_index:13,created_at:"2025-08-16T14:14:06"}
  ],
  dailyProgress: [
    {id:266,subject_id:1,date:"2025-07-01",completed_count:100,created_at:"2025-08-16T14:14:09"},
    {id:267,subject_id:1,date:"2025-07-15",completed_count:150,created_at:"2025-08-16T14:14:09"},
    {id:268,subject_id:1,date:"2025-08-01",completed_count:200,created_at:"2025-08-16T14:14:09"},
    {id:269,subject_id:2,date:"2025-07-01",completed_count:10,created_at:"2025-08-16T14:14:09"},
    {id:270,subject_id:2,date:"2025-07-15",completed_count:25,created_at:"2025-08-16T14:14:09"},
    {id:271,subject_id:2,date:"2025-08-01",completed_count:40,created_at:"2025-08-16T14:14:09"},
    {id:272,subject_id:3,date:"2025-07-01",completed_count:20,created_at:"2025-08-16T14:14:09"},
    {id:273,subject_id:3,date:"2025-07-15",completed_count:50,created_at:"2025-08-16T14:14:09"},
    {id:274,subject_id:3,date:"2025-08-01",completed_count:80,created_at:"2025-08-16T14:14:09"},
    {id:275,subject_id:10,date:"2025-07-01",completed_count:100,created_at:"2025-08-16T14:14:09"},
    {id:276,subject_id:10,date:"2025-07-15",completed_count:300,created_at:"2025-08-16T14:14:09"},
    {id:277,subject_id:10,date:"2025-08-01",completed_count:500,created_at:"2025-08-16T14:14:09"},
    {id:278,subject_id:11,date:"2025-07-01",completed_count:150,created_at:"2025-08-16T14:14:09"},
    {id:279,subject_id:11,date:"2025-07-15",completed_count:350,created_at:"2025-08-16T14:14:09"},
    {id:280,subject_id:11,date:"2025-08-01",completed_count:600,created_at:"2025-08-16T14:14:09"}
  ]
};

localStorage.setItem('studySubjects', JSON.stringify(importData.subjects));
localStorage.setItem('studyProgress', JSON.stringify(importData.dailyProgress));
console.log('✅ データインポート完了！');
location.reload();
```

5. **ページが自動的にリロードされ、データが表示されます**

---

## 方法3: JSONファイルを使用

1. **メインアプリを開く**
   https://yuzu1128.github.io/Yuzu-project/

2. **「データ管理」ボタンをクリック**

3. **「データインポート」セクションで**
   - https://yuzu1128.github.io/Yuzu-project/import-data.json をダウンロード
   - ファイルを選択
   - 「データを読み込む」をクリック

---

## 確認方法

インポート後、以下を確認：
- ✅ 13科目が表示される
- ✅ 各科目の進捗が正しい
- ✅ グラフにデータが反映される

## エラーが続く場合

ブラウザのキャッシュをクリア：
- Windows: `Ctrl+Shift+Delete`
- Mac: `Cmd+Shift+Delete`

それでも解決しない場合は、別のブラウザでお試しください。