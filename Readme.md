## topics

* Timescaledb


## Karthi Table:

CREATE TABLE tm_trac_tbl (

    jn_id SERIAL PRIMARY KEY,

    vhe_id INT NOT NULL,

    drv_id INT NOT NULL,

    start_loc VARCHAR(255) NOT NULL,

    end_loc VARCHAR(255) NOT NULL,

    start_time TIMESTAMP NOT NULL,

    end_time TIMESTAMP,

    cur_loc VARCHAR(255),

    status_id INT NOT NULL,

    dist_tvl DECIMAL(10, 2),

    est_ariv TIMESTAMP,

    last_update_time TIMESTAMP NOT NULL,

    FOREIGN KEY (vhe_id) REFERENCES tr_vhe_tbl(vhe_id),

    FOREIGN KEY (drv_id) REFERENCES driver(drv_id),

    FOREIGN KEY (status_id) REFERENCES status(status_id)

);