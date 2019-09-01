# Multimarkdown Crack

> IDEA 插件 markdown-navigator 破解版



## 声明

> 如果有能力的话建议还是选择支持正版，本项目主要用于本人的学习交流使用

## 使用教程

1. 点击下面的连接，下载插件文件

   [下载连接](https://github.com/gclm/Share/releases/download/multimarkdown-2.9.7/idea-multimarkdown-2.9.7-gclm.zip)

2. 导入并重启IDEA

3. 打开设置看见如下图所示则说明该软件已经破解成功了

   ![](https://gitee.com/gclm/img/raw/master/20190831234521-xIdHZt.jpg)

## 破解教程

### 1. 下载插件安装包

-  [官网下载](https://plugins.jetbrains.com/plugin/7896-markdown-navigator/versions)
- IDEA 内下载

> 推荐使用官网下载

### 2. 创建项目

1. 建议创建如下的项目结构

   ![](https://gitee.com/gclm/img/raw/master/20190831235849-OH9QWD.jpg)
2. 解压上步下载的 idea-multimarkdown-XXX.zip 文件，把lib重命名为 multimarkdown_lib，放到项目文件中   

### 3. 修改项目

```bash
# 1. 重命名idea-multimarkdown.jar 为 `idea-multimarkdown.bak.jar` 作为备份，并 copy 文件到 releases/2.9.7 中
# 2. 解压插件
cd releases/2.9.7
# 解压到 source 文件夹(没找到解压到指定文件夹的参数...)
cp idea-multimarkdown.bak.jar ./source/
cd source
jar xvf idea-multimarkdown.bak.jar && rm -f idea-multimarkdown.bak.jar
# 将要修改的 LicenseAgent.java 拷贝到上面创建的包里
cd 你的项目目录
cp releases/2.9.7/source/com/vladsch/idea/multimarkdown/license/LicenseAgent.java crack/src/com/vladsch/idea/multimarkdown/license/
```

### 4. 修改授权文件，修改为以下格式
```java
/*
 * Copyright (c) 2015-2018 Vladimir Schneider <vladimir.schneider@gmail.com>, all rights reserved.
 *
 * This code is private property of the copyright holder and cannot be used without
 * having obtained a license or prior written permission of the of the copyright holder.
 *
 * Unless required by applicable law or agreed to in writing,
 * software distributed under the License is distributed on an
 * "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
 * KIND, either express or implied.  See the License for the
 * specific language governing permissions and limitations
 * under the License.
 *
 */
package com.vladsch.idea.multimarkdown.license;

import com.intellij.openapi.diagnostic.Logger;
import org.jetbrains.annotations.NotNull;
import org.jetbrains.annotations.Nullable;

import javax.json.JsonObject;
import java.util.HashMap;
import java.util.Map;

public class LicenseAgent {
    private static final Logger logger = Logger.getInstance("com.vladsch.idea.multimarkdown.license.agent");

    // RELEASE : set to false for release
    private static final boolean LOG_AGENT_INFO = false;

    final static private String agent_signature = "475f99b03f6ec213729d7f5d577c80aa";
    final static private String license_pub = "-----BEGIN PUBLIC KEY-----\n" +
            "MIICIjANBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKCAgEAlnefMGqNu1Q9hcI2Rd8G\n" +
            "xyKlXQIFyXWIkYODRrLjvEwXYw0yksgjZeIC4g+hakyQNiN+TGE/xvo3fqB0CU4A\n" +
            "aE33Mu7jB27dt1IItcmBhJBwIhmZDc0SWNj6ywvnLeUU/NSWWbJ1SaXzPQJ2Mm5T\n" +
            "Mr3wDFhCTp80pN4svOQmdQPFSKXwdGI+n8gJvc28vRgD8As2XxgkYsZPNjefOsla\n" +
            "GHS8CNw6uI8Ijcf9hfX22twQZ+auYNL/vqtBEKq2jNLwoHTo68s+0JWJu2YILlIe\n" +
            "VQzXcXZyhhAVdZrMNGhBPiXUia6YrJpqZNDZ35CE+Y6ecs9c5AG2wpFJHnic2cjZ\n" +
            "Kh+ba83DpA3GxYa1OGMGZNaIqCjuK7A82ZPriXsoxL6YJzqSlbF/2l2x4Y3VoVTF\n" +
            "LWKEpjvLOuDOev0CH41nzkGD4Yo5CwHPZFun/WekqUBUXtxR/uH0ThoxV93exTLc\n" +
            "YwWC5GqVZfN38Ye7iDljIFVzxxP3unBy0FItg52407CZyH/gTB+Zm++fZJdKbZcl\n" +
            "UFvxtACEJvdgdM30FHuQlvS53mEXOMAzpJPVZu2gRoTl8cSO3GKxaNP9dmPCzD4a\n" +
            "gO/kVrO/c6DerwWvCJJhifKlDc6CfjM3FfWsVI2gw3WduFPJcIsLxlUqzBh95rA1\n" +
            "R+BTr2n3DV41OK5AwtCQO40CAwEAAQ==\n" +
            "-----END PUBLIC KEY-----\n";

    final static private String licenseHeader = "-----BEGIN MARKDOWN-NAVIGATOR LICENSE-----";
    final static private String licenseFooter = "-----END MARKDOWN-NAVIGATOR LICENSE-----";
    final static private String activationHeader = "-----BEGIN MARKDOWN-NAVIGATOR ACTIVATION-----";
    final static private String activationFooter = "-----END MARKDOWN-NAVIGATOR ACTIVATION-----";
    final static private String altLicenseHeader = "-----BEGIN IDEA-MULTIMARKDOWN LICENSE-----";
    final static private String altLicenseFooter = "-----END IDEA-MULTIMARKDOWN LICENSE-----";
    final static private String altActivationHeader = "-----BEGIN IDEA-MULTIMARKDOWN ACTIVATION-----";
    final static private String altActivationFooter = "-----END IDEA-MULTIMARKDOWN ACTIVATION-----";

    // RELEASE : comment out DEV LICENSE SERVER
    final static public String siteURL = "https://vladsch.com";
    final static public String authSiteURL = "auth.vladsch.com";
    final static public String auth1SiteURL = "vladsch.com";
    final static public String auth2SiteURL = "dev.vladsch.com";

    // DEBUG : debug site and licensing URLs
    //final static public String siteURL = "http://vladsch.dev";
    //final static public String authSiteURL = "vladsch.dev";
    //final static public String auth1SiteURL = authSiteURL;
    //final static public String auth2SiteURL = authSiteURL;

    final static public String diagnosticSiteURL = auth1SiteURL;
    final static public String diagnostic1SiteURL = authSiteURL;
    final static public String diagnostic2SiteURL = auth2SiteURL;

    final static public String productPrefixURL = "/product/markdown-navigator";
    final static public String altProductPrefixURL = "/product/multimarkdown";
    final static public String patchRelease = siteURL + productPrefixURL + "/patch-release";
    final static public String eapRelease = siteURL + productPrefixURL + "/eap-release";
    final static public String altPatchRelease = siteURL + altProductPrefixURL + "/patch-release";
    final static public String altEapRelease = siteURL + altProductPrefixURL + "/eap-release";

    final static private String licenseURL = authSiteURL + productPrefixURL + "/json/license";
    final static private String alt1LicenseURL = auth1SiteURL + productPrefixURL + "/json/license";
    final static private String alt2LicenseURL = auth2SiteURL + productPrefixURL + "/json/license";

    final static public String tryPageURL = siteURL + productPrefixURL + "/try";
    final static public String buyPageURL = siteURL + productPrefixURL + "/buy";
    final static public String specialsPageURL = siteURL + productPrefixURL + "/specials";
    final static public String productPageURL = siteURL + productPrefixURL;
    final static public String referralsPageURL = siteURL + productPrefixURL + "/referrals";

    final static public String feedbackURL = diagnosticSiteURL + productPrefixURL + "/json/diagnostic";
    final static public String feedbackURL1 = diagnostic1SiteURL + productPrefixURL + "/json/diagnostic";
    final static public String statusURL = diagnosticSiteURL + productPrefixURL + "/json/diagnostic-status";
    final static public String statusURL1 = diagnostic1SiteURL + productPrefixURL + "/json/diagnostic-status";

    private static final String ACTIVATION_EXPIRES = "activation_expires";
    private static final String LICENSE_EXPIRES = "license_expires";
    private static final String PRODUCT_VERSION = "product_version";
    private static final String PRODUCT_RELEASED_AT = "product_released_at";
    private static final String AGENT_SIGNATURE = "agent_signature";
    private static final String LICENSE_CODE = "license_code";
    private static final String LICENSE_TYPE = "license_type";
    private static final String LICENSE_FEATURES = "license_features";
    private static final String LICENSE_FEATURE_LIST = "feature_list";
    private static final String ACTIVATION_CODE = "activation_code";
    private static final String HOST_PRODUCT = "host_product";
    private static final String HOST_NAME = "host_name";
    private static final String ACTIVATED_ON = "activated_on";
    private static final String STATUS = "status";
    private static final String MESSAGE = "message";
    private static final String STATUS_DISABLE = "disable";
    private static final String STATUS_OK = "ok";
    private static final String STATUS_ERROR = "error";
    private static final String DATE_FORMAT = "yyyy-MM-dd";

    public static final String LICENSE_TYPE_TRIAL = "trial";
    public static final String LICENSE_TYPE_SUBSCRIPTION = "subscription";
    public static final String LICENSE_TYPE_LICENSE = "license";

    private String license_code;
    private String activation_code;
    private JsonObject activation;
    private String license_expires;
    private String product_released_at;
    private String product_version;
    private JsonObject json; // last server response
    private boolean remove_license;
    private String license_type;
    private int license_features;
    private Map<String, Integer> featureList = new HashMap<>();
    private String lastCommunicationsError = null;
    private boolean isSecureConnection = true;

    public Map<String, Integer> getFeatureList() {
        return featureList;
    }

    public LicenseAgent(LicenseAgent other) {
        copyFrom(other);
    }

    public boolean isSecureConnection() {
        return isSecureConnection;
    }

    public void setSecureConnection(boolean secureConnection) {
        isSecureConnection = secureConnection;
    }

    public void copyFrom(LicenseAgent other) {
        this.license_code = other.license_code;
        this.activation_code = other.activation_code;
        this.activation = other.activation;
        this.license_expires = other.license_expires;
        this.product_released_at = other.product_released_at;
        this.product_version = other.product_version;
        this.json = other.json;
        this.remove_license = other.remove_license;
        this.license_type = other.license_type;
        this.license_features = other.license_features;
        this.featureList = other.featureList;
        this.isSecureConnection = other.isSecureConnection;
        this.lastCommunicationsError = other.lastCommunicationsError;
    }

    public boolean isRemoveLicense() {
        return remove_license;
    }

    @NotNull
    public static String getTrialLicenseURL() {
        return tryPageURL;
    }

    /**
     * 不设置任何东西
     */
    public void setLicenseCode(String license_code) {
    }

    /**
     * 不设置任何东西
     */
    public void setLicenseActivationCodes(String license_code, String activation_code) {
    }

    /**
     * 不设置任何东西
     */
    public void setActivationCode(String activation_code) {
    }

    @NotNull
    public static String getLicenseURL() {
        return buyPageURL;
    }

    @NotNull
    public String licenseCode() {
        return license_code != null ? license_code : "";
    }

    /**
     * 改过期时间
     * @return
     */
    @Nullable
    public String getLicenseExpires() {
        return "9999-12-31";
    }

    @Nullable
    public String getProductVersion() {
        return product_version;
    }

    @NotNull
    public String getMessage() {
        String message;
        return json != null ? ((message = json.getString(MESSAGE)) != null ? message : "") : "";
    }

    @Nullable
    public String getStatus() {
        return json != null ? json.getString(STATUS) : null;
    }

    @NotNull
    public String activationCode() {
        return activation_code != null ? activation_code : "";
    }

    @Nullable
    public JsonObject getActivation() {
        return activation;
    }

    @Nullable
    public String getLastCommunicationsError() {
        return lastCommunicationsError;
    }

    /**
     * 添加功能
     */
    public LicenseAgent() {
        featureList = new HashMap<>();
        featureList.put("enhanced", 1);
        featureList.put("development", 2);
    }

    /**
     * 直接返回 true
     */
    public boolean getLicenseCode(LicenseRequest licenseRequest) {
        return true;
    }

    /**
     * 直接返回 true
     */
    public boolean isValidLicense() {
        return true;
    }

    /**
     * 直接返回 true
     */
    public boolean isValidActivation() {
        return true;
    }

    /**
     * 修改为具体值
     */
    @NotNull
    public String getLicenseType() {
        return LICENSE_TYPE_LICENSE;
    }

    /**
     * 修改为具体值
     */
    public int getLicenseFeatures() {
        return LicensedFeature.Feature.LICENSE.getLicenseFlags();
    }

    /**
     * 设置到期日
     */
    @NotNull
    public String getLicenseExpiration() {
        return "9999-12-31";
    }

    @NotNull
    public String getHostName() {
        if (activation != null && activation.containsKey(HOST_NAME)) {
            return activation.getString(HOST_NAME);
        }
        return "";
    }

    @NotNull
    public String getHostProduct() {
        if (activation != null && activation.containsKey(HOST_PRODUCT)) {
            return activation.getString(HOST_PRODUCT);
        }
        return "";
    }

    /**
     * 设置注册日期
     */
    @NotNull
    public String getActivatedOn() {
        return "2018-01-01";
    }

    /**
     * 设置剩余天数
     */
    public int getLicenseExpiringIn() {
        return Integer.MAX_VALUE;
    }

    public boolean getProductIsPerpetual() {
        // see if the license is valid because product is perpetually licensed
        return getLicenseExpiringIn() <= 0;
    }

    public static int floorDiv(int var0, int var1) {
        int var2 = var0 / var1;
        if ((var0 ^ var1) < 0 && var2 * var1 != var0) {
            --var2;
        }

        return var2;
    }

    public static long floorDiv(long var0, long var2) {
        long var4 = var0 / var2;
        if ((var0 ^ var2) < 0L && var4 * var2 != var0) {
            --var4;
        }

        return var4;
    }

    /**
     * 直接返回否：未过期
     * @return
     */
    public boolean isActivationExpired() {
        return false;
    }
}
```

### 5. 添加依赖编译文件
打开 LicenseAgent.java 文件你会发现很多报错，无法编译，是因为没有依赖包

编译前首先需要引入 IDEA 和 multimarkdown 的依赖包

IDEA 依赖包在 IDEA 安装目录中

![](https://gitee.com/gclm/img/raw/master/20190901000727-hf9Y4L.jpg)

multimarkdown 的依赖包在该插件目录中

![](https://gitee.com/gclm/img/raw/master/20190901000846-r1urUz.jpg)

导入依赖后菜单 Build → Build Project 编译项目
然后会生成 out 目录，编译好的 .class 文件就在这里

### 6. 重新打包

```bash
#1. 将修改后的 LicenseAgent.class 文件拷贝到解压后的 jar 包中
cp LicenseAgent.class ./releases/2.9.7/source/com/vladsch/idea/multimarkdown/license/
#2. 重新打包并移到上层目录
cd releases/2.9.7/source && jar cvf idea-multimarkdown.jar * && mv idea-multimarkdown.jar ../

# 3. 将打好的包拷贝到第一步下载的 IDEA 插件目录中覆盖掉原文件
```

### 7. 将插件导入IDEA 中

看见以下效果，则说明破解完成

 ![](https://gitee.com/gclm/img/raw/master/20190831234521-xIdHZt.jpg)
