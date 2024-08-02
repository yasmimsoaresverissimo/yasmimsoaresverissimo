INSERT INTO public.tbl_estado
(estado_id, nome)
VALUES(gen_random_uuid(), 'AM');

SELECT estado_id, nome
FROM public.tbl_estado;

INSERT INTO public.tbl_cidade
(cidade_id, nome, estado_estado_id)
VALUES(gen_random_uuid(), 'MPU', '');

SELECT estado_id, nome
FROM public.tbl_estado;

INSERT INTO public.tbl_orgao
(orgao_id, active, endereco_cep, nome, endereco_cidade_id)
VALUES(gen_random_uuid(), true, 'BR', 'MEC', '');

SELECT orgao_id, active, endereco_cep, nome, endereco_cidade_id
FROM public.tbl_orgao;

INSERT INTO public.tbl_departamento
(departamento_id, active, orgao_id, nome, sigla, unidade_pai, localidade)
VALUES(uuid_generate_v4(), true,'af7de58d-7c58-4f9b-9579-2c7c49cb4815', 'EDUCAÇÃO', 'SEEC', 'AM', 'BRASIL');

SELECT departamento_id, active, orgao_id, nome, sigla, unidade_pai, localidade
FROM public.tbl_departamento;

SELECT movement_id, date_time_final, date_time_create, pessoa_recebedora_id, subscritor_id, tipo_movimentacao, mobil_mobil_id
FROM public.tbl_movement;

SELECT mark_id, code, desc_detalhada, nome, tipo_marca
FROM public.tbl_mark;

SELECT mobil_id, mark_id
FROM public.marca_mobil_adicionada;

SELECT user_id, active, nome, "password", matricula, email, department_id, telefone, endereco, rg, cpf
FROM public.tbl_user;

SELECT role_id, role_type
FROM public.tbl_roles;

INSERT INTO public.tbl_mark(mark_id, code, desc_detalhada, nome, tipo_marca)VALUES(uuid_generate_v4(), 0, '', '', 0);

INSERT INTO public.tbl_mark(mark_id, code, desc_detalhada, nome, tipo_marca)VALUES(uuid_generate_v4(), 0, 'Criação', 'CRIACAO', 0);

INSERT INTO public.tbl_mark(mark_id, code, desc_detalhada, nome, tipo_marca)VALUES(uuid_generate_v4(), 1, 'Assinar com senha', 'ASSINAR_COM_SENHA', 1);

INSERT INTO public.tbl_mark(mark_id, code, desc_detalhada, nome, tipo_marca)VALUES(uuid_generate_v4(), 2, 'Inclusão de conssignatário', 'INCLUSAO_COSSIGNATARIO', 2);

INSERT INTO public.tbl_mark(mark_id, code, desc_detalhada, nome, tipo_marca)VALUES(uuid_generate_v4(), 3, 'Tramitação de documento', 'TRAMITACAO_DOCUMENTO', 3);

INSERT INTO public.tbl_mark(mark_id, code, desc_detalhada, nome, tipo_marca)VALUES(uuid_generate_v4(), 4, 'FINALIZACAO', 'FINALIZAR', 4);

SELECT user_id, role_id
FROM public.tbl_users_roles;

SELECT mobil_id, subscritor_id, date_create, desc_detalhada, sigla_mobil, ult_movimentacao_id, documento_document_id
FROM public.tbl_mobil;

INSERT INTO public.tbl_users_roles
(user_id, role_id)
VALUES('57ad0f65-8076-4549-b65f-2b83aab6ad27', '28406496-07e6-4a1e-9bcc-70f481e5f946');

SELECT mobil_id, subscritor_id, date_create, desc_detalhada, sigla_mobil, ult_movimentacao_id, documento_document_id
FROM public.tbl_mobil;

INSERT INTO public.tbl_model
(model_id, date_time_final, descricao_detalhada, html_form, html_model_doc, "label", sigla)
VALUES(uuid_generate_v4(), NOW(), 'Memorando é um tipo de documento que trata assuntos internos.', 'Assunto

                                                                              <label class="form-label">Interessado</label>
                                                                              <input type="text" class="form-control" id="Interessado">
                                                                              <div id="emailHelp" class="form-text">Informe o interessado.</div>

                                                                              <label for="documentBody" class="form-label">Descrição</label>
                                                                              <textarea class="form-control" id="documentBody" rows="3"></textarea>', '<!DOCTYPE html>
                                                                                          <html lang="en">
                                                                                          <head>
                                                                                              <meta charset="UTF-8">
                                                                                              <meta name="viewport" content="width=device-width, initial-scale=1.0">
                                                                                              <title>Modelo Memorando</title>
                                                                                              <style>

                                                                                                  * {
                                                                                                      margin: 0;
                                                                                                      box-sizing: border-box;
                                                                                                  }

                                                                                                  .VisualizadorDocumento {
                                                                                                      width: 100%;
                                                                                                      padding: 10px;
                                                                                                      border: 1px solid #5c5c5c;
                                                                                                      margin: 0 auto;
                                                                                                  }

                                                                                                  .MargemDocumento {
                                                                                                      max-width: 900px;
                                                                                                      margin: 0 auto;
                                                                                                  }

                                                                                                  .LogoDocumento {
                                                                                                      text-align: center;
                                                                                                      margin-top: 50px;
                                                                                                      margin-bottom: 50px;
                                                                                                  }

                                                                                                  .LogoDocumento img {
                                                                                                      max-width: 100px;
                                                                                                  }

                                                                                                  .DataLocalCriacaoDocumento {
                                                                                                      text-align: right;
                                                                                                  }

                                                                                                  .InformacoesDocumento {
                                                                                                      text-align: center;
                                                                                                      margin-top: 100px;
                                                                                                      margin-bottom: 100px;
                                                                                                  }

                                                                                                  .InformacoesDocumento b,
                                                                                                  .InformacoesDocumento p {
                                                                                                      margin: 0;
                                                                                                      padding: 0;
                                                                                                  }

                                                                                                  .CorpoDocumento {
                                                                                                      text-align: left;
                                                                                                  }

                                                                                                  .CorpoDocumento p {
                                                                                                      margin: 0;
                                                                                                      padding: 0;
                                                                                                      white-space: pre-wrap;
                                                                                                      overflow-wrap: break-word;
                                                                                                  }

                                                                                                  .RodapeDocumento {
                                                                                                      text-align: center;
                                                                                                      margin-top: 80px;
                                                                                                      margin-bottom: 80px;
                                                                                                  }

                                                                                                  .RodapeDocumento p {
                                                                                                      margin: 0;
                                                                                                      padding: 0;
                                                                                                      white-space: pre-wrap;
                                                                                                      overflow-wrap: break-word;
                                                                                                  }

                                                                                              </style>
                                                                                          </head>
                                                                                          <body>
                                                                                              <div class="VisualizadorDocumento" id="VisualizadorDocumento">
                                                                                                  <div class="MargemDocumento" id="MargemDocumento">
                                                                                                      <div class="LogoDocumento" id="LogoDocumento">
                                                                                                          <img src="https://seeklogo.com/images/P/prefeitura-de-manacapuru-logo-2FBDF8B79C-seeklogo.com.png" alt="Logo do documento">
                                                                                                      </div><!--LogoDocumento-->

                                                                                                      <div class="DataLocalCriacaoDocumento" id="DataLocalCriacaoDocumento">
                                                                                                          <p>DataCriacaoDocumento</p>
                                                                                                      </div><!--DataLocalCriacaoDocumento-->

                                                                                                      <div class="InformacoesDocumento" id="InformacoesDocumento">
                                                                                                          <b>#Orgao</b>
                                                                                                          <p>#SecretariaCriacaoDocumento</p>
                                                                                                      </div><!--DataLocalCriacaoDocumento-->

                                                                                                      <div class="CorpoDocumento" id="CorpoDocumento">
                                                                                                          <p><b>Número de referência: </b>NumeroReferencia</p>
                                                                                                          <p><b>Interessado: </b>Interessado</p>
                                                                                                          <p><b>Descrição: </b>Descricao</p>
                                                                                                      </div><!--CorpoDocumento-->

                                                                                                      <div class="RodapeDocumento" id="RodapeDocumento">
                                                                                                          <b>#PessoaAssinante</b>
                                                                                                          <p>#SecretariaPessoaAssinante</p>
                                                                                                          <p>#DataAssinatura</p>
                                                                                                      </div><!--RodapeDocumento-->
                                                                                                  </div><!--MargemDocumento-->
                                                                                              </div><!--VisualizadorDocumento-->

                                                                                          </body>
                                                                                          </html>
', 'Memorando', 'MEM');

