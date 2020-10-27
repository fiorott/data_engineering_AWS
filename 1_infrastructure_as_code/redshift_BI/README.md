# Integrating Redshift with a BI tool

The process of connecting Redshift to a BI tool is always very similar, regardless of the tool you use.
Here we will use [Metabase] (https://www.metabase.com/start/oss/) with Docker.

``
docker run -d -p 3000: 3000 --name metabase metabase / metabase
``

1. Access Metabase at `localhost: 3000`
1. Get your Redshift host on the AWS panel (remember that the password and username are hardcoded in the Redshift template for now)
1. In step 3 of the Metabase configuration, add your data.
! [] (metabase.png)
1. Create your queries and dashboards!