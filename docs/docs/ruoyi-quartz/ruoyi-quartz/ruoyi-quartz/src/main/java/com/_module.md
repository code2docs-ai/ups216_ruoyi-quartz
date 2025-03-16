# 基础信息

|      |      |
|------|------|
| 编码语言 | .java |
| 代码路径 | ruoyi-quartz/ruoyi-quartz/src/main/java/com |
| 包名 | ruoyi-quartz.ruoyi-quartz.src.main.java.com |
| 概述说明 | JobInvokeUtil类解析调用方法，CronUtils处理Cron表达式，Quartz任务类管理定时任务，RyTask类处理多类型参数，SysJobController管理任务，SysJobLogController处理日志，SysJobServiceImpl和SysJobLogServiceImpl实现任务和日志管理，SysJobLog和SysJob类记录任务属性和日志。 |

# 说明

JobInvokeUtil类负责解析并调用目标方法及其参数，简化任务执行流程。CronUtils类处理Cron表达式，验证合法性并获取执行时间。抽象类处理Quartz任务，自动记录日志并包含异常处理机制。QuartzJobExecution类继承自AbstractQuartzJob，重写doExecute方法并调用JobInvokeUtil.invokeMethod。Quartz任务类确保任务不并发执行，通过调度器管理任务触发。ScheduleUtils类管理定时任务，提供任务创建和触发策略设置。RyTask类包含三个方法，分别处理多类型参数、字符串参数和无参数。SysJobController管理定时任务，提供查看、导出、删除、修改状态等功能。SysJobLogController处理调度日志相关操作，包括查看、导出、删除和清理。SysJobServiceImpl类管理定时任务，包括初始化、查询、暂停、恢复等功能。SysJobLogServiceImpl类提供日志查询、新增、删除和清空功能。SysJobLog类记录任务日志，包含ID、任务名、调用目标等属性。SysJob类用于任务管理，包含任务ID、名称、执行表达式等属性。


### 包内部结构视图

```mermaid
graph TD
    com --> ruoyi
    ruoyi --> quartz
    quartz --> util
    quartz --> task
    quartz --> controller
    quartz --> service
    quartz --> domain
    quartz --> config
    quartz --> mapper
    util --> JobInvokeUtil.java
    util --> CronUtils.java
    util --> AbstractQuartzJob.java
    util --> QuartzJobExecution.java
    util --> QuartzDisallowConcurrentExecution.java
    util --> ScheduleUtils.java
    task --> RyTask.java
    controller --> SysJobController.java
    controller --> SysJobLogController.java
    service --> impl
    service --> ISysJobService.java
    service --> ISysJobLogService.java
    impl --> SysJobServiceImpl.java
    impl --> SysJobLogServiceImpl.java
    domain --> SysJobLog.java
    domain --> SysJob.java
    config --> ScheduleConfig.java
    mapper --> SysJobLogMapper.java
    mapper --> SysJobMapper.java
```

该流程图展示了ruoyi-quartz项目中Java代码的层级结构。从`com`目录开始，逐步深入到`ruoyi`和`quartz`目录，最终展示出`util`、`task`、`controller`、`service`、`domain`、`config`和`mapper`等子目录及其包含的具体文件。每个节点代表路径的最后一级元素，清晰地反映了项目的组织结构。

# 文件列表 File List

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [ruoyi](ruoyi/_module.md) | package | JobInvokeUtil类解析调用方法，CronUtils处理Cron表达式，Quartz任务类管理定时任务，RyTask类处理多类型参数，SysJobController管理任务，SysJobLogController处理日志，SysJobServiceImpl和SysJobLogServiceImpl实现任务和日志管理，SysJobLog和SysJob类记录任务属性和日志。 |
| [ruoyi](ruoyi/_module.md) | package | JobInvokeUtil类解析调用方法，CronUtils处理Cron表达式，Quartz任务类管理定时任务，RyTask类处理多类型参数，SysJobController管理任务，SysJobLogController处理日志，SysJobServiceImpl和SysJobLogServiceImpl实现任务和日志管理，SysJobLog和SysJob类记录任务属性和日志。 |


