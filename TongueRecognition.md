# 1 前言
## 1.1 需求背景
未来使用者通过手机或相机拍摄的舌象（舌面、舌根）照片上传系统，本舌象识别、诊断系统根据预先建立的神经网络模型进行图像的分类，判断用户舌象属性，并给出健康建议，辅助客户进行自诊断或者就医参考。

 
# 2 系统设计要点和思路
本系统的核心基于机器学习中深度学习的思想进行核心模型的构建，基于JavaEE技术实现。机器学习（Machine Learning）是一种从实例样本数据或过去的经验中进行学习，以优化某种性能指标并建立相关模型，以获取相关知识或技能，然后借助该模型用于未知样本的推理指导，是人工智能的核心研究领域之一。其具体过程为：训练特征数据或以往经验来建立相关模型并通过先验知识循环优化模型中的参数，从而预测新的数据，从该数据中获取知识。
深度学习（deep learning）是机器学习的子领域，是试图通过一系列多层的非线性的变换对数据进行抽象的算法。深度学习通过模拟具有丰富层次结构的脑神经系统，建立类似于人脑的分层模型结构，对输入数据逐级提取，形成更加抽象的高层表示（属性类别或特征）。深度学习利用多层非线性信息处理来实现有监督或者无监督的特征提取和转换、模式分析和分类，用来解释如图像、声音、文本的数据。高层次的特征和概念，根据较低层次的特征和概念来定义，相同低层次的概念可用来定义很多高层次的概念。这样一个分层次的结构称为深层结构，主要有两个关键方面：（1）模型由多层次或阶段的非线性信息处理组成；（2）特征表示的有监督或无监督学习，随着层数的提高，而更加抽象。深度学习使用了分层抽象的思想，高层的概念通过低层的概念学习得到。
硬件的进步也是深度学习重新受到关注的重要因素，随着计算机芯片的处理能力大幅提高，高性能图形图像处理器（GPUs）的出现大大提升了数值和矩阵运算的速度，使得机器学习算法的运行时间明显地缩短了，另外，硬件计算的成本显著降低，机器学习和信号/信息处理研究的进步，都使得深度学习研究迅速发展

# 3 主要功能点列表
## 3.1 舌象识别深度学习训练模型
## 3.2 舌苔照片采集和预处理
用户基于手机或PC端将拍照后的舌象照片上传系统。照片要符合指定的一些标准（如像素点的要求），系统提供图像预处理功能，以便进行图像规范化和统一化，提高分类的准确度数据的处理过程包括数据的预处理、特征提取和选择。数据预处理的目的是加强有用的信息，改善图像质量，便于对图像进行分析和处理。特征提取是用映射（或变换）的方法将高维空间的原始特征变换为低维空间的新特征，从而有利于分类。
## 3.3 舌苔照片识别和分析
基于训练好的分类模型对上传的舌象照片进行分析并分类，确定所分析的舌象照片的多重属性，如舌色、舌形、舌态、苔色等，并给出分类结果供后续诊断使用。
## 3.4 舌象诊断和分析
根据图像识别以及分类结果，系统根据内置的推理规则生成针对当前用户舌象照片的分类给出分析建议和报告。如果用户需要文件，系统自动生成PDF、DOC等格式，并提供系统接口、下载功能、文件传输接口。
## 3.5 用户舌苔数据综合分析
将用户所上传的多幅舌象图像按照不同维度进行分类、展示、综合分析和对比等。并提供综合分析报告，供客户下载或者其他系统接口使用
## 3.6 舌象库管理
对用户的舌象以及对应的属性进行管理，包括增加、删除和修改等。同时提供系统内置的已经分类好的各种舌苔图片提供展示，并提供各种舌苔的症状和建议的处理方案，以供用户了解学习
## 3.7 用户信息管理
管理用户的个人基础信息，包括用户信息的增删改查，权限管理等。
## 3.8 数据安全与访问控制
系统管理员的功能，包括数据备份、导入导出、访问权限控制、访问日志等。
## 3.9 系统后台管理
常规系统后台管理，例如数据字典、操作日志、用户权限配置等。

 

# 4 设计约束和质量控制
## 4.1 设计约束
1. 编程语言和编程限制：编程语言为java，特定情况下使用C/C++。
2. 对两款软件进行单元测试、单元集成和测试、配置项测试。软件产品应参加软硬件集成测试、系统联试，软件承办方需提供软硬件集成测试和系统联试中的技术支持、软件完善。
## 4.2 质量控制要求
### 4.2.1 标准
采用面向对象技术进行软件开发、测试。
### 4.2.2 文档
软件开发文档清单及评审要求按软件工程规范执行，具体内容作为未来协议附件。
### 4.2.3 配置管理
系统开发使用SVN作为CM工具，使用Jira或者其他合适软件作为Bug Track工具。
### 4.2.4 测试要求
本软件应进行单元测试、集成测试、配置项测试。组织软硬件集成测试、系统联试。开发过程提供完整的测试数据、流程和说明。 
