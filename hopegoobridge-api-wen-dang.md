# HopegooBridge API文档

## 目录

1. **存储操作 (Storage Operations)**
   * [saveStorage (保存数据)](broken-reference)
   * [getStorage (获取数据)](broken-reference)
   * [deleteStorage (删除数据)](broken-reference)
2. **照片操作 (Photo Operations)**
   * [getPhotoFromAlbum (从相册获取照片)](broken-reference)
   * [notifyCropPhoto (裁剪照片通知)](broken-reference)
   * [openCamera (打开相机)](broken-reference)
3. **通用工具 (General Tools)**
   * [getLocation (获取定位)](broken-reference)
   * [setAnalysis (设置埋点)](broken-reference)
   * [changeLang (更改语言)](broken-reference)
   * [getAppThemeColor (获取应用主题色)](broken-reference)
   * [getDeviceInfo (获取设备信息)](broken-reference)
   * [openNewUrl (打开新URL)](broken-reference)
   * [navigateBack (导航返回)](broken-reference)
   * [postMessage (发送消息)](broken-reference)
   * [dataCallback (数据回调)](broken-reference)
4. **网络请求 (Network Requests)**
   * [networkRequest (网络请求)](broken-reference)
5. **账户操作 (Account Operations)**
   * [getLoginInfo (获取登录信息)](broken-reference)
   * [bindAccount (绑定账户)](broken-reference)
   * [wakeUpLogin (唤醒登录)](broken-reference)
6. **导航栏操作 (Navigation Operations)**
   * [setNavigate (设置导航栏)](broken-reference)
   * [getNavigateHeight (获取导航栏高度)](broken-reference)

***

## 存储操作 (Storage Operations)

### saveStorage (保存数据)

保存数据到本地存储。

* **参数**:
  * `key` (String): 存储键名。
  * `value` (Object): 存储数据。
*   **示例**:

    ```javascript
    HopegooBridge.saveStorage('userKey', { name: 'John' }, response => {
      console.log(response);
    });
    ```

### getStorage (获取数据)

从本地存储获取数据。

* **参数**:
  * `key` (String): 存储键名。
*   **示例**:

    ```javascript
    HopegooBridge.getStorage('userKey', response => {
      console.log(response);
    });
    ```

### deleteStorage (删除数据)

删除本地存储中的数据。

* **参数**:
  * `key` (String): 存储键名。
*   **示例**:

    ```javascript
    HopegooBridge.deleteStorage('userKey', response => {
      console.log(response);
    });
    ```

***

## 照片操作 (Photo Operations)

### getPhotoFromAlbum (从相册获取照片)

从相册中选择照片。

*   **示例**:

    ```javascript
    HopegooBridge.getPhotoFromAlbum(response => {
      console.log(response);
    });
    ```

### notifyCropPhoto (裁剪照片通知)

通知应用裁剪选定的照片。

*   **示例**:

    ```javascript
    HopegooBridge.notifyCropPhoto(response => {
      console.log(response);
    });
    ```

### openCamera (打开相机)

打开相机进行拍照。

*   **示例**:

    ```javascript
    HopegooBridge.openCamera(response => {
      console.log(response);
    });
    ```

***

## 通用工具 (General Tools)

### getLocation (获取定位)

获取当前设备的地理位置信息。

* **示例**:

```javascript
 HopegooBridge.getLocation(response => {
   console.log(response);
 });
```

### setAnalysis (设置埋点)

发送分析或埋点信息。

* **参数**:
  * `event` (String): 事件名称。
  * `data` (Object): 事件数据。
*   **示例**:

    ```javascript
    HopegooBridge.setAnalysis('clickEvent', { buttonId: 'btn123' }, response => {
      console.log(response);
    });
    ```

### changeLang (更改语言)

更改应用的显示语言。

* **参数**:
  * `language` (String): 目标语言。
*   **示例**:

    ```javascript
    HopegooBridge.changeLang('en-US', response => {
      console.log(response);
    });
    ```

### getAppThemeColor (获取应用主题色)

获取当前应用的主题颜色。

*   **示例**:

    ```javascript
    HopegooBridge.getAppThemeColor(response => {
      console.log(response);
    });
    ```

### getDeviceInfo (获取设备信息)

获取当前设备的详细信息。

*   **示例**:

    ```javascript
    HopegooBridge.getDeviceInfo(response => {
      console.log(response);
    });
    ```

### openNewUrl (打开新URL)

在新标签页中打开一个URL。

* **参数**:
  * `url` (String): 目标URL。
*   **示例**:

    ```javascript
    HopegooBridge.openNewUrl('https://www.example.com', response => {
      console.log(response);
    });
    ```

### navigateBack (导航返回)

导航回上一个页面。

*   **示例**:

    ```javascript
    HopegooBridge.navigateBack();
    ```

### postMessage (发送消息)

向原生应用发送消息。

* **参数**:
  * `message` (Object): 消息内容。
*   **示例**:

    ```javascript
    HopegooBridge.postMessage({ key: 'value' }, response => {
      console.log(response);
    });
    ```

### dataCallback (数据回调)

接收原生应用的数据回调。

*   **示例**:

    ```javascript
    HopegooBridge.dataCallback(response => {
      console.log(response);
    });
    ```

***

## 网络请求 (Network Requests)

### networkRequest (网络请求)

发起网络请求。

* **参数**:
  * `options` (Object): 请求参数。
*   **示例**:

    ```javascript
    const requestParams = {
      method: 'GET',
      url: 'https://api.example.com/data'
    };
    HopegooBridge.networkRequest(requestParams, response => {
      console.log(response);
    });
    ```

***

## 账户操作 (Account Operations)

### getLoginInfo (获取登录信息)

获取当前用户的登录信息。

*   **示例**:

    ```javascript
    HopegooBridge.getLoginInfo(response => {
      console.log(response);
    });
    ```

### bindAccount (绑定账户)

绑定用户账户。

*   **示例**:

    ```javascript
    HopegooBridge.bindAccount(response => {
      console.log(response);
    });
    ```

### wakeUpLogin (唤醒登录)

唤起登录界面。

*   **示例**:

    ```javascript
    HopegooBridge.wakeUpLogin(response => {
      console.log(response);
    });
    ```

***

## 导航栏操作 (Navigation Operations)

### setNavigate (设置导航栏)

设置应用的导航栏。

* **参数**:
  * `params` (Object): 导航栏设置。
*   **示例**:

    ```javascript
    const navSettings = {
      title: 'My Page',
      iconType: 'back'
    };
    HopegooBridge.setNavigate(navSettings, response => {
      console.log(response);
    });
    ```

### getNavigateHeight (获取导航栏高度)

获取应用导航栏的高度。

*   **示例**:

    ```javascript
    HopegooBridge.getNavigateHeight(response => {
      console.log(response);
    });
    ```
