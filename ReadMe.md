##反向代理服务：

做成war包的 反向代理服务。   可用于tomcat中。 测试 好用，get post 上传图片等。ok  
  
参考  https://github.com/mitre/HTTP-Proxy-Servlet#smileys-http-proxy-servlet  

   
    <servlet>  
        <servlet-name>solr</servlet-name>  
        <servlet-class>org.mitre.dsmiley.httpproxy.ProxyServlet</servlet-class>  
        <init-param>  
          <param-name>targetUri</param-name>  
          <param-value>http://solrserver:8983/solr</param-value>  
        </init-param>  
        <init-param>  
          <param-name>log</param-name>  
          <param-value>true</param-value>  
        </init-param>  
    </servlet>  
    <servlet-mapping>  
      <servlet-name>solr</servlet-name>  
      <url-pattern>/solr/*</url-pattern>  
    </servlet-mapping>  
   
配置在 web.xml中。
