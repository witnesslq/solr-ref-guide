# 客户端APIs简介

Solr 的本质是一个 Web 应用，但因为它建立在开放的协议上，任何类型的客户端应用都可以使用 Solr。

HTTP 是客户端应用和 Solr 之间的基本协议。客户端发送请求然后 Solr 做一些事情并提供一个响应。
客户端使用请求来让 Solr 完成像执行查询或索引文档这样的事情。

客户端应用可以通过创建 HTTP 请求和解析 HTTP 响应来接触 Solr。
客户端 APIs 封装了很多发送请求和解析响应的工作，使得可以更容易地编写客户端应用。

客户端使用 Solr 的五个基本操作来使用 Solr。这些操作有查询、索引、删除、提交和优化。

查询通过创建一个包含所有查询参数的 URL 来执行。
Solr 会检查请求的 URL，执行该查询并返回结果。
其他操作也类似，只是某些情况下 HTTP 请求是一个 POST 操作，
且包含了一些不在请求 URL 中的信息。
比如说索引操作可以在请求体中包含一个文档。

Solr 也有一个 `EmbeddedSolrServer` 特性，它提供了不需要 HTTP 连接的 Java API。
更多信息，查看 [使用SolrJ](./solrj.md)。
