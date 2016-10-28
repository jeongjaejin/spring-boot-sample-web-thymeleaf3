# spring-boot-sample-web-thymeleaf3

Issue Report - Using Thymeleaf Layout Dialect.

<pre>
	<table id="t1">
	  <colgroup>
	    <col /> <!-- here! -->
	  </colgroup>
	  <tr><td>1</td></tr>
	</table>
	<table id="t2">
	  <colgroup>
	    <col /> <!-- here! -->
	  </colgroup>
	  <tr><td>2</td></tr>
	</table>
</pre>
Two table with colgroup & col tags in one layout fragment appear under exception.

Exception: 
2016-10-28 13:41:35.074 ERROR 16132 --- [nio-8080-exec-9] o.a.c.c.C.[.[.[/].[dispatcherServlet]    : Servlet.service() for servlet [dispatcherServlet] in context with path [] threw exception [Request processing failed; nested exception is org.thymeleaf.exceptions.TemplateInputException: An error happened during template parsing (template: "class path resource [templates/messages/list.html]")] with root cause

org.thymeleaf.exceptions.TemplateProcessingException: Cannot set containing close tag to skip when model level is zero
	at org.thymeleaf.engine.TemplateModelController.skipCloseTag(TemplateModelController.java:307) ~[thymeleaf-3.0.2.RELEASE.jar:3.0.2.RELEASE]
	at org.thymeleaf.engine.TemplateModelController.skip(TemplateModelController.java:293) ~[thymeleaf-3.0.2.RELEASE.jar:3.0.2.RELEASE]
	at org.thymeleaf.engine.ProcessorTemplateHandler.handleOpenElement(ProcessorTemplateHandler.java:1594) ~[thymeleaf-3.0.2.RELEASE.jar:3.0.2.RELEASE]
	at org
