# elasticsearch-analysis-ik
要实现IK对特殊字符的支持，只要修改2处地方即可

第一处：
elasticsearch-analysis-ik-6.2.3/src/main/java/org/wltea/analyzer/core/CharacterUtil.java   
目的是让它能识别出这些特殊字符，涉及46和71行。

第二处：
elasticsearch-analysis-ik-6.2.3/src/main/java/org/wltea/analyzer/core/AnalyzeContext.java  
目的是不让这些特殊字符单独输出成为索引，涉及58和300行。

此项目属于被修改后重新打包过的，直接使用target下的elasticsearch-analysis-ik-6.2.3.jar覆盖es项目中plugins/ik文件夹下的指定文件，重启ES即可。