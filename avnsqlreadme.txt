SQL Commands
------------

SELECT  *FROM avn;

ALTER TABLE public.avn ADD COLUMN tnum bigint default nextval('ticket_sequence'::regclass) PRIMARY KEY;

ALTER TABLE avn ADD COLUMN statuss  varchar(100);

CREATE TABLE public.avn(
  tnum bigint default nextval('ticket_sequence'::regclass),
  other_column TEXT
);


INSERT INTO public.avn(product, pdesc, cont, datee, statuss ) VALUES ('DIGITALTV', 'NW Issue','9884970793','15/03/2017','OPEN' ) RETURNING *;
INSERT INTO public.avn(pdesc) VALUES ('NOT WORKING') RETURNING *;
INSERT INTO public.avn(cont) VALUES ('9884570793') RETURNING *;
INSERT INTO public.avn(datee) VALUES ('20/03/2017') RETURNING *;
INSERT INTO public.avn(statuss) VALUES ('NEW ') RETURNING *;

delete FROM public.avn;

username
