FROM mariadb:10.5

ADD Server/utils/sql/database_full/quarm_2024-08-25-18_09.tar.gz /docker-entrypoint-initdb.d
RUN rm /docker-entrypoint-initdb.d/drop_system.sql

ADD Server/loginserver/login_util/tblloginserversettings.sql /docker-entrypoint-initdb.d
ADD Server/loginserver/login_util/updates/2023_07_27_tblLoginServerAccounts.sql /docker-entrypoint-initdb.d/x_2023_07_27_tblLoginServerAccounts.sql

ADD containers/database/update_settings.sql /docker-entrypoint-initdb.d/0_update_settings.sql
ADD containers/database/update_quarm.sql /docker-entrypoint-initdb.d/z_update_quarm.sql
