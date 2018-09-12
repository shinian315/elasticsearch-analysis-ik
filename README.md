# elasticsearch-analysis-ik
要实现IK对特殊字符的支持，只要修改2处地方即可
elasticsearch-analysis-ik-6.2.3/src/main/java/org/wltea/analyzer/core/CharacterUtil.java   （目的是让它能识别出这些特殊字符）
elasticsearch-analysis-ik-6.2.3/src/main/java/org/wltea/analyzer/core/AnalyzeContext.java  （目的是不让这些特殊字符单独输出成为索引）
