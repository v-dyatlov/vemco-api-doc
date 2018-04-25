FORMAT: 1A

# VemcountAPI

# Reports [/api/shop]
Shop resource representation

## Get shop data [GET /api/shop/{ids}]
Get a JSON data of Shop.

+ Parameters
    + ids: (string, required) - List of Shop IDs divided by comma, for example: /api/shop/1,2,3

# Reports [/api/reports]
Reports resource representation

## Get report data [POST /api/reports]
Get a JSON representation of Report based on parameters.

+ Parameters
    + source: (string, required) - Report source<br/>
     *     locations, groups, zones, sensors
    + data[]: (integer, required) - ID of the source, you can add few parameters `data[]` to request
    + data_output[]: (string, required) - Data outputs (for example `count_in`, `turnover` etc.), you can add few parameters `data_output[]` to request
    + period[]: (string, optional) - Period of your report, you can add few parameters `period[]` to request<br/>
     *     yesterday, today, this_week, last_week, this_month, last_month, this_quarter, last_quarter, this_year, last_year, date 
        + Default: yesterday
    + period_step: (string, optional) - Period step of data<br/>
     *     15min, 30min, hour, day, week, month, quarter, year, total
        + Default: hour
    + show_hours_from: (string, optional) - Report hours from, in 24h format
        + Default: 08:00
    + show_hours_to: (string, optional) - Report hours to, in 24h format
        + Default: 20:00
    + opening_hours_overlap: (integer, optional) - Opening hours overlap. If this option selected, then time goes after midnight, for example: 20:00 - 08:00
        + Default: 0
    + show_days[]: (integer, optional) - List of available weekdays. 0 - Sunday, 6 - Saturday
        + Default: All the days are enabled
    + show_months[]: (integer, optional) - List of available months. 1 - January, 12 - December
        + Default: All the months are enabled
