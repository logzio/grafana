+++
title = "What's New in Grafana v5.1"
description = "Feature & improvement highlights for Grafana v5.1"
keywords = ["grafana", "new", "documentation", "5.1"]
type = "docs"
[menu.docs]
name = "Version 5.1"
identifier = "v5.1"
parent = "whatsnew"
weight = -7
+++

# What's New in Grafana v5.1

Grafana v5.1 brings many enhancements and bug fixes to Prometheus, Cloudwatch, PostgreSQL, MySQL, alerting, graph, table and singlestat panels. It also adds support for Microsft SQL Server as metric & table data source!

## Prometheus

New enhancements includes support for Prometheus histograms in the heatmap panel and autocomplete of template variables query editor. More information in the [Prometheus data source docs](/features/datasources/prometheus/).

## Cloudwatch

New enhancements includes support for high resolution metrics and dimension filtering. More information in the [Cloudwatch data source docs](/features/datasources/cloudwatch/).

## PostgreSQL

New enhancement includes support for filling in values for missing intervals and better precision handling and data type support for time columns. More information in the [PostgreSQL data source docs](/features/datasources/postgres/#time-series-queries).

## MySQL

New enhancements includes support for filling in values for missing intervals, better precision handling and data type support for time columns and any column except time and metric is now treated as a value column. More information in the [MySQL data source docs](/features/datasources/mysql/#time-series-queries).

## Microsoft SQL Server

Grafana v5.1 now ships with a built-in Microsoft SQL Server (MSSQL) data source plugin that allows you to query and visualize data from any Microsoft SQL Server 2005 or newer, including Microsoft Azure SQL Database. Have logs or metric data in MSSQL? You can now visualize that data and
define alert rules on it like any of our other data sources.

Same enhancements as for PostgreSQL and MySQL have been incorporated for MSSQL as well. More information in the [Microsoft SQL Server data source docs](/features/datasources/mssql/).

{{< docs-imagebox img="/img/docs/v51/mssql_query_editor.png"  max-width= "800px" >}}

## Provisioning



## Alerting

New enhancements includes support for retries on failed alert queries and updating correct state when pausing/un alerts.

## Graph Panel

New enhancements includes support for multiple series stacking in histogram mode, thresholds for right Y axis, aligning left and right Y-axes to one level and additional units. More information in the [Graph panel docs](/features/panels/graph/).

## Table Panel

New enhancements includes support for mapping a numeric value/range to text and additional units. More information in the [Table panel docs](/features/panels/table_panel/#string).

## Singlestat Panel

New enhancements includes support for adding color to prefix and postfix and additional units. More information in the [Singlestat panel docs](/features/panels/singlestat/).

## Changelog

### New Features

* **MSSQL**: New Microsoft SQL Server data source [#10093](https://github.com/grafana/grafana/pull/10093), [#11298](https://github.com/grafana/grafana/pull/11298), thx [@linuxchips](https://github.com/linuxchips)
* **Prometheus**: The heatmap panel now support Prometheus histograms [#10009](https://github.com/grafana/grafana/issues/10009)
* **Postgres/MySQL**: Ability to insert 0s or nulls for missing intervals [#9487](https://github.com/grafana/grafana/issues/9487), thanks [@svenklemm](https://github.com/svenklemm)
* **Postgres/MySQL/MSSQL**: Fix precision for the time column in table mode [#11306](https://github.com/grafana/grafana/issues/11306)
* **Graph**: Align left and right Y-axes to one level [#1271](https://github.com/grafana/grafana/issues/1271) &  [#2740](https://github.com/grafana/grafana/issues/2740) thx [@ilgizar](https://github.com/ilgizar)
* **Graph**: Thresholds for Right Y axis [#7107](https://github.com/grafana/grafana/issues/7107), thx [@ilgizar](https://github.com/ilgizar)
* **Graph**: Support multiple series stacking in histogram mode [#8151](https://github.com/grafana/grafana/issues/8151), thx [@mtanda](https://github.com/mtanda)
* **Alerting**: Pausing/un alerts now updates new_state_date [#10942](https://github.com/grafana/grafana/pull/10942)
* **Alerting**: Support Pagerduty notification channel using Pagerduty V2 API [#10531](https://github.com/grafana/grafana/issues/10531), thx [@jbaublitz](https://github.com/jbaublitz)
* **Templating**: Add comma templating format [#10632](https://github.com/grafana/grafana/issues/10632), thx [@mtanda](https://github.com/mtanda)
* **Prometheus**: Show template variable candidate in query editor [#9210](https://github.com/grafana/grafana/issues/9210), thx [@mtanda](https://github.com/mtanda)
* **Prometheus**: Support POST for query and query_range [#9859](https://github.com/grafana/grafana/pull/9859), thx [@mtanda](https://github.com/mtanda)
* **Alerting**: Add support for retries on alert queries [#5855](https://github.com/grafana/grafana/issues/5855), thx [@Thib17](https://github.com/Thib17)
* **Table**: Table plugin value mappings [#7119](https://github.com/grafana/grafana/issues/7119), thx [infernix](https://github.com/infernix)
* **IE11**: IE 11 compatibility [#11165](https://github.com/grafana/grafana/issues/11165)
* **Scrolling**: Better scrolling experience [#11053](https://github.com/grafana/grafana/issues/11053), [#11252](https://github.com/grafana/grafana/issues/11252), [#10836](https://github.com/grafana/grafana/issues/10836), [#11185](https://github.com/grafana/grafana/issues/11185), [#11168](https://github.com/grafana/grafana/issues/11168)

### Minor changes

* **OpsGenie**: Add triggered alerts as description [#11046](https://github.com/grafana/grafana/pull/11046), thx [@llamashoes](https://github.com/llamashoes)
* **Cloudwatch**: Support high resolution metrics [#10925](https://github.com/grafana/grafana/pull/10925), thx [@mtanda](https://github.com/mtanda)
* **Cloudwatch**: Add dimension filtering to CloudWatch `dimension_values()` [#10029](https://github.com/grafana/grafana/issues/10029), thx [@willyhutw](https://github.com/willyhutw)
* **Units**: Second to HH:mm:ss formatter [#11107](https://github.com/grafana/grafana/issues/11107), thx [@gladdiologist](https://github.com/gladdiologist)
* **Singlestat**: Add color to prefix and postfix in singlestat panel [#11143](https://github.com/grafana/grafana/pull/11143), thx [@ApsOps](https://github.com/ApsOps)
* **Dashboards**: Version cleanup fails on old databases with many entries [#11278](https://github.com/grafana/grafana/issues/11278)
* **Server**: Adjust permissions of unix socket [#11343](https://github.com/grafana/grafana/pull/11343), thx [@corny](https://github.com/corny)
* **Shortcuts**: Add shortcut for duplicate panel [#11102](https://github.com/grafana/grafana/issues/11102)
* **AuthProxy**: Support IPv6 in Auth proxy white list [#11330](https://github.com/grafana/grafana/pull/11330), thx [@corny](https://github.com/corny)
* **SMTP**: Don't connect to STMP server using TLS unless configured. [#7189](https://github.com/grafana/grafana/issues/7189)
* **Prometheus**: Escape backslash in labels correctly. [#10555](https://github.com/grafana/grafana/issues/10555), thx [@roidelapluie](https://github.com/roidelapluie)
* **Variables**: Case-insensitive sorting for template values [#11128](https://github.com/grafana/grafana/issues/11128) thx [@cross](https://github.com/cross)
* **Annotations (native)**: Change default limit from 10 to 100 when querying api [#11569](https://github.com/grafana/grafana/issues/11569), thx [@flopp999](https://github.com/flopp999)
* **MySQL/Postgres/MSSQL**: PostgreSQL datasource generates invalid query with dates before 1970 [#11530](https://github.com/grafana/grafana/issues/11530) thx [@ryantxu](https://github.com/ryantxu)
* **Kiosk**: Adds url parameter for starting a dashboard in inactive mode [#11228](https://github.com/grafana/grafana/issues/11228), thx [@towolf](https://github.com/towolf)
* **Dashboard**: Enable closing timepicker using escape key [#11332](https://github.com/grafana/grafana/issues/11332)
* **Datasources**: Rename direct access mode in the data source settings [#11391](https://github.com/grafana/grafana/issues/11391)
* **Search**: Display dashboards in folder indented [#11073](https://github.com/grafana/grafana/issues/11073)
* **Units**: Use B/s instead Bps for Bytes per second [#9342](https://github.com/grafana/grafana/pull/9342), thx [@mayli](https://github.com/mayli)
* **Units**: Radiation units [#11001](https://github.com/grafana/grafana/issues/11001), thx [@victorclaessen](https://github.com/victorclaessen)
* **Units**: Timeticks unit [#11183](https://github.com/grafana/grafana/pull/11183), thx [@jtyr](https://github.com/jtyr)
* **Units**: Concentration units and "Normal cubic metre" [#11211](https://github.com/grafana/grafana/issues/11211), thx [@flopp999](https://github.com/flopp999)
* **Units**: New currency - Czech koruna [#11384](https://github.com/grafana/grafana/pull/11384), thx [@Rohlik](https://github.com/Rohlik)
* **Avatar**: Fix DISABLE_GRAVATAR option [#11095](https://github.com/grafana/grafana/issues/11095)
* **Heatmap**: Disable log scale when using time time series buckets [#10792](https://github.com/grafana/grafana/issues/10792)
* **Provisioning**: Remove `id` from json when provisioning dashboards, [#11138](https://github.com/grafana/grafana/issues/11138)
* **Prometheus**: tooltip for legend format not showing properly [#11516](https://github.com/grafana/grafana/issues/11516), thx [@svenklemm](https://github.com/svenklemm)

### Tech
* Migrated JavaScript files to TypeScript
