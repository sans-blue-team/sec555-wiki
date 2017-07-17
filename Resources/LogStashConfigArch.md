SEC555: LogStash Config Numbering Architecture
======

Logstash Naming Logic
------
Logstash can load a single configuration file or multiple. In production environments, it is recommended to seperate configuration files into seperate pieces. Doing this and using a standard naming convention provides many advantages such as:

1. Less code writeen/code reuse
2. Standardized field enrichment
3. Simplified configuration administration

Config Numbering Graphic
------
The initial recommendation is to use the below numbering schemese with your log files. The scheme uses four digit numbers at the beginning of each configuration file where the first number specifies what the configuration file function is intended for.

>   ![](./media/image1.png)



**Warning:** **\*** Post processing assumes standardized field names such as **src\_ip**, **id.orig\_h, ip.src** renamed to **source\_ip**

SEC555 LogStash Configs
------

### **SEC555 VM**
> LogStash config files are stored on SEC555VM at: **`/opt/Logstash-Configs/configfiles`**

### **GitHub**
> Justin Henderson's (@SecurityMapper) LogStash Configs on GitHub:
> <https://github.com/SMAPPER/Logstash-Configs/tree/master/configfiles>
