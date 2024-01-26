# Yomamabeenlama
Completely worthless 
{
  "formatVersion": 1,
  "database": {
    "version": 1,
    "identityHash": "af24c4a8bbe69965d004d506dce3a90f",
    "entities": [
      {
        "tableName": "notification_schedules",
        "createSql": "CREATE TABLE IF NOT EXISTS `${TABLE_NAME}` (`id` TEXT NOT NULL, `day_of_week` INTEGER NOT NULL, `starts_at` TEXT NOT NULL, `ends_at` TEXT NOT NULL, PRIMARY KEY(`day_of_week`))",
        "fields": [
          {
            "fieldPath": "id",
            "columnName": "id",
            "affinity": "TEXT",
            "notNull": true
          },
          {
            "fieldPath": "day",
            "columnName": "day_of_week",
            "affinity": "INTEGER",
            "notNull": true
          },
          {
            "fieldPath": "startsAt",
            "columnName": "starts_at",
            "affinity": "TEXT",
            "notNull": true
          },
          {
            "fieldPath": "endsAt",
            "columnName": "ends_at",
            "affinity": "TEXT",
            "notNull": true
          }
        ],
        "primaryKey": {
          "columnNames": [
            "day_of_week"
          ],
          "autoGenerate": false
        },
        "indices": [],
        "foreignKeys": []
      },
      {
        "tableName": "analytics_events",
        "createSql": "CREATE TABLE IF NOT EXISTS `${TABLE_NAME}` (`uuid` INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL, `app_element` TEXT NOT NULL, `app_action` TEXT NOT NULL, `performed_at` TEXT NOT NULL, `subject_type` TEXT, `context` TEXT)",
        "fields": [
          {
            "fieldPath": "uuid",
            "columnName": "uuid",
            "affinity": "INTEGER",
            "notNull": true
          },
          {
            "fieldPath": "appElement",
            "columnName": "app_element",
            "affinity": "TEXT",
            "notNull": true
          },
          {
            "fieldPath": "appAction",
            "columnName": "app_action",
            "affinity": "TEXT",
            "notNull": true
          },
          {
            "fieldPath": "performedAt",
            "columnName": "performed_at",
            "affinity": "TEXT",
            "notNull": true
          },
          {
            "fieldPath": "subjectType",
            "columnName": "subject_type",
            "affinity": "TEXT",
            "notNull": false
          },
          {
            "fieldPath": "context",
            "columnName": "context",
            "affinity": "TEXT",
            "notNull": false
          }
        ],
        "primaryKey": {
          "columnNames": [
            "uuid"
          ],
          "autoGenerate": true
        },
        "indices": [],
        "foreignKeys": []
      }
    ],
    "views": [],
    "setupQueries": [
      "CREATE TABLE IF NOT EXISTS room_master_table (id INTEGER PRIMARY KEY,identity_hash TEXT)",
      "INSERT OR REPLACE INTO room_master_table (id,identity_hash) VALUES(42, 'af24c4a8bbe69965d004d506dce3a90f')"
    ]
  }
}