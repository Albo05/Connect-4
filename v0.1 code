//
//  ViewController.swift
//  Connect!4
//
//  Created by Alberto Fantinato on 31/10/22.
//

import UIKit

class ViewController: UIViewController {

    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.
    }
    
    var tabella = [[0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0]]
    var turno : Int32 = 0

    func vittoria() -> Bool {
        if(orizzontale() || verticale() || vittoriaDiagonale()){
            return true
        }
        return false
    }
    func orizzontale() -> Bool{
        for righe in tabella{
            var diFila = 0
            for colonne in righe{
                if(colonne == turno){
                    diFila += 1
                    if(diFila >= 4){
                        return true
                    }
                }
                else{
                    diFila = 0
                }
            }
        }
        return false
    }
    func verticale() -> Bool{
        for colonna in 0...tabella.count{
            var diFila = 0
            for riga in tabella{
                if(riga[colonna] == turno){
                    diFila += 1
                    if(diFila >= 4){
                        return true
                    }
                }
                else{
                    diFila = 0
                }
            }
        }
        return false
    }
    func vittoriaDiagonale() -> Bool{
        for colonna in 0...tabella.count{
            if (diagonale(colonna, true, true)){
                return true
            }
            if (diagonale(colonna, true, false)){
                return true
            }
            if (diagonale(colonna, false, true)){
                return true
            }
            if (diagonale(colonna, false, false)){
                return true
            }
        }
        return false
    }
    func diagonale(_ colonnaDaControllare: Int,_ vuoiAndareSu: Bool,_ roverso: Bool) -> Bool{
        var colonneMuoventi = colonnaDaControllare
        var diFila = 0
        if(roverso){
            for riga in tabella.reversed(){
                if colonneMuoventi < riga.count && colonneMuoventi >= 0{
                    if riga[colonneMuoventi] == turno{
                        diFila += 1
                        if(diFila >= 4){
                            return true
                        }
                    }
                    else{
                        diFila = 0
                    }
                    colonneMuoventi = vuoiAndareSu ? colonneMuoventi + 1 : colonneMuoventi - 1
                }
            }
        }
        else{
            for riga in tabella.reversed(){
                if colonneMuoventi < riga.count && colonneMuoventi >= 0{
                    if riga[colonneMuoventi] == turno{
                        diFila += 1
                        if(diFila >= 4){
                            return true
                        }
                    }
                    else{
                        diFila = 0
                    }
                    colonneMuoventi = vuoiAndareSu ? colonneMuoventi + 1 : colonneMuoventi - 1
                }
            }
        }
        return false
    }
}

