---
{
    "title": "EXISTS 操作符",
    "language": "zh-CN"
}
---

<!-- 
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
-->

## 描述

EXISTS 条件用于测试子查询中行的存在性。

## 操作符介绍

| 操作符 | 作用                                    | 示例                                                         |
| ------ | --------------------------------------- | ------------------------------------------------------------ |
| EXISTS | 如果子查询返回至少一条数据，则返回 TRUE | `SELECT department_id  FROM departments d  WHERE EXISTS  (SELECT * FROM employees e    WHERE d.department_id    = e.department_id)   ORDER BY department_id;` |