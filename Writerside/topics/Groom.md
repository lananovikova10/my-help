# Groom

### Groom Projects Query

<link-summary>
    Query for the groom_projects table.
</link-summary>

```SQL
SELECT gp.project_id,
       gp.project_id_auto_sequence,
       gp.project_name,
       get_enum(p_enum_name => 'ProjectStatus', p_sys_value_name => gp.enum_project_status) AS project_status,
       NEW_TIME(gp.default_cut_over_date, 'GMT', get_timezone()) AS default_cut_over_date,
```